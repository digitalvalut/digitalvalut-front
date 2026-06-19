# DigitalValut — Modello dei costi AI (token)

> Documento di lavoro. Risponde alla domanda critica: **a €19/mese, chi paga i token
> che consumano i clienti?** Spoiler: con l'architettura giusta sono spiccioli, e il
> rischio "utente pesante" si neutralizza con un tetto. Da rifinire insieme.

---

## 0. Il principio che abbatte i costi

Dal Reliability Brief: **l'LLM fa solo linguaggio, il codice fa i calcoli.** L'AI non
"ragiona tanto" — interpreta la domanda, chiama il motore deterministico, formatta la
risposta. Quindi **non serve un modello costoso**: basta un modello piccolo ed economico.

---

## 1. Prezzi di riferimento (per milione di token)

| Modello | Input | Output | Quando usarlo |
|---|---|---|---|
| **Claude Haiku 4.5** | $1 | $5 | Default per il layer linguistico — perfetto |
| Claude Sonnet 4.6 | $3 | $15 | Solo se serve più qualità di spiegazione |
| Modelli open (Llama, Mistral, DeepSeek via OpenRouter) | ~$0,1–0,5 | ~$0,2–0,6 | Massimo risparmio |

**OpenRouter** è un gateway (routing + fail-over multi-modello): utile per flessibilità,
ma **non rende i token più economici** — paghi il prezzo del modello + una piccola fee.
Il risparmio vero viene dal modello piccolo + il caching (sotto).

---

## 2. La leva chiave: prompt caching

Il system prompt fiscale è lungo e **identico a ogni richiesta**. Con il prompt caching:
- la prima volta lo paghi pieno (scrittura cache: 1,25×),
- le riletture costano **~0,1× (un decimo)** → fino al **90% di risparmio** sulla parte
  ripetuta.
Si ammortizza già dalla 2ª richiesta.

---

## 3. I conti veri (a €19/mese)

Tipica domanda fiscale ≈ 3.000 token input + 500 output. Con Haiku 4.5 + caching attivo:

| Scenario | Costo/interazione | 200 domande/mese | 500 domande/mese |
|---|---|---|---|
| Haiku 4.5 + caching | ~$0,002–0,005 | **~$1** | **~$2,5** |
| Modelli open (OpenRouter) | ~$0,001 | **<$1** | **~$1** |

> A €19/mese restano **~17–18 € di margine lordo** sui token. L'economia regge largamente.

---

## 4. Il rischio "utente pesante" — e come si blocca

Il pericolo non è l'utente medio, ma chi fa migliaia di richieste lunghe. Si neutralizza
con **una** di queste (standard nei SaaS con AI):

1. **Fair-use / quota** — il tier €19 include es. "300 domande AI/mese"; oltre, si rallenta
   o si fa upgrade.
2. **Crediti AI** — €19 = pacchetto crediti; il pesante ne compra altri.
3. **BYOK (Bring Your Own Key)** — l'utente pesante collega la *sua* chiave: **paga lui i
   suoi token**. Rischio nostro = zero.

---

## 5. Il bivio che conta più dei costi: locale vs cloud ⚠️

Il nostro posizionamento e il Reliability Brief promettono *"i dati restano nello studio"*.
Mandare la chat a un cloud (OpenRouter) **violerebbe** quella promessa. Due strade:

| | **A) Modello locale/open** *(consigliata)* | **B) Cloud (OpenRouter)** |
|---|---|---|
| Privacy | ✅ Dati non escono dallo studio | ❌ Dati al cloud — va dichiarato |
| Costo token | Quasi zero (gira su tua macchina/server) | Basso ma non nullo |
| Coerenza col pitch | ✅ Totale | ⚠️ Da gestire con disclaimer |
| Complessità tecnica | Più alta (deploy modello locale) | Più bassa (chiamata API) |

**Raccomandazione:** **opzione A** o un **ibrido** — calcoli e dati sensibili in locale; il
cloud (se mai) solo per spiegazioni generiche e con dati anonimizzati. La privacy è
l'identità del prodotto: meglio non barattarla per comodità tecnica.

---

## 6. Break-even (esempio)

Con costo token ~$1–2,5/cliente/mese e prezzo €19/mese, il margine lordo per cliente è
~€16–17. Coprire ~€500/mese di costi fissi richiede **~30 clienti paganti**. (Stima da
rifinire con i costi reali del team.)

---

## 7. Prossimo passo

1. Scegliere **A (locale)** o **B (cloud)** — cambia numeri e promessa privacy.
2. Impostare **un tetto di fair-use** dal giorno 1 (anche solo "300 domande/mese").
3. Attivare il **prompt caching** sul system prompt (risparmio immediato ~90%).
