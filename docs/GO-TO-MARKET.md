# DigitalValut — Piano di vendita (Go-To-Market)

> Documento di lavoro. Scenario: piccolo team di **sviluppatori**, prodotto **usabile**,
> **nessuna rete commerciale**, nessun venditore. Obiettivo: vendere senza diventare
> commercianti. Da rifinire insieme.

---

## 0. Il principio guida

Il nostro punto debole non è il prodotto: è la **distribuzione**. Quindi la strategia
non è "imparare a vendere porta a porta", ma **scegliere canali che non richiedono una
rete commerciale**. Due leve:

1. **Self-serve** — il prodotto si vende online da solo (prova → carta → attivazione).
2. **Un partner di canale non esclusivo** — qualcuno che ha già la rete, mentre il
   self-serve cresce.

Non si sceglie l'una O l'altra: si parte con la prima e si aggiunge la seconda.

---

## 1. Posizionamento (contro Genya / TeamSystem)

Non competiamo come "gestionale completo": là perdiamo (no integrazioni, no rete, no brand).
Competiamo sulla **fessura** che i giganti non possono coprire:

| Loro (Genya, TeamSystem) | Noi (DigitalValut) |
|---|---|
| AI a "scatola chiusa" | Ogni numero **tracciabile**: fonte datata + golden test |
| Dati sul cloud del fornitore | Dati che **non escono dallo studio** (privacy by design) |
| Prezzo a preventivo, opaco | **Prezzo pubblico e chiaro** sul sito |
| Ecosistema costoso e lento | Focalizzato, economico, evolve in fretta |

**Messaggio guida:** *"Non fidarti dell'AI: verifica la fonte di ogni cifra. Trasparente
sul calcolo, trasparente sul prezzo."*

**Modalità d'ingresso consigliata:** non sostituire il gestionale, ma **affiancarlo** come
*controllo di qualità / secondo parere verificabile* sui calcoli critici. Basso attrito:
non chiediamo a nessuno di abbandonare ciò che già usa.

---

## 2. Prezzo

Sfruttiamo il nostro vero vantaggio: costo marginale per cliente bassissimo (motore locale).
Modello **SaaS, abbonamento mensile per utente** (no licenza una-tantum).

| Tier | Prezzo | Quando usarlo |
|---|---|---|
| **Penetrazione** | ~19 €/mese/utente (~190–230 €/anno) | Partenza: massimizzare adozione, non margine |
| **Verifica affidabile** | ~40–60 €/mese (~500–700 €/anno) | Affianca il gestionale come secondo parere |
| **Premium privacy** | ~80–120 €/mese (~1.000–1.400 €/anno) | Solo con referenze e prove (più avanti) |

Riferimenti di mercato: TeamSystem base ~1.000 €+/anno, entry ~1.900 €/anno; Genya a
preventivo (~1.500–4.000+ €/anno stimati). **Siamo 1/5–1/10 del costo.** È un argomento.

**Tattica:** primi mesi gratis/scontati per i "pionieri" in cambio di feedback e referenza.

---

## 3. Self-serve vs Distributore — i numeri

| | Self-serve (diretto) | Distributore / rivenditore |
|---|---|---|
| Margine trattenuto | ~100% (meno costi infra/pagamenti ~5%) | ~50–70% (loro prendono 30–50%) |
| Velocità di accesso clienti | Lenta (mesi) | Rapida (settimane) |
| Controllo cliente/dati | Pieno | Indiretto |
| Sforzo commerciale nostro | Marketing online | Gestione partner |
| Rischio | Crescita lenta | **Esclusiva = dipendenza** |

**Regola d'oro:** mai concedere **esclusiva nazionale** all'inizio. Se proprio, esclusiva
**solo territoriale e a tempo**, legata a obiettivi minimi di vendita.

---

## 4. Come trovare i primi 10 clienti (senza venditori)

I primi clienti li porta il **fondatore**, non una rete. Tattiche da sviluppatori:

1. **Rete calda:** ogni commercialista che già conosciamo (il nostro, amici, famiglia).
   Obiettivo: 3–5 demo nelle prime 2 settimane.
2. **Una sola killer-demo:** mostrare il **bug IMU 100 vs 160** risolto e tracciabile.
   "Il tuo software ti fa vedere *perché* esce questo numero? Il nostro sì."
3. **Contenuti tecnici:** 1 post/articolo che spiega un errore fiscale reale e come lo
   rendiamo impossibile. Pubblicato dove stanno i commercialisti (LinkedIn, gruppi,
   forum di categoria). Attira da solo.
4. **Ordini professionali locali (Crotone/Calabria e oltre):** webinar gratuito di 30 min
   a un Ordine dei Dottori Commercialisti. Un solo "sì" = una sala piena di prospect.
5. **Programma referral:** ogni studio che ne porta un altro ha sconto. Il passaparola tra
   commercialisti vale più di qualsiasi pubblicità.

Target: **10 studi paganti** prima di pensare a scalare o a un distributore.

---

## 5. Piano 90 giorni

**Giorni 0–30 — Fondamenta**
- [ ] Sito con **prezzo pubblico**, pagina "perché siamo verificabili", prova gratuita.
- [ ] Pagamento self-serve (Stripe o simile) + attivazione automatica.
- [ ] Killer-demo registrata (caso IMU tracciabile).
- [ ] Lista di 30 commercialisti da contattare (rete calda + locali).

**Giorni 30–60 — Primi clienti**
- [ ] 5–10 demo dal vivo; primi 3–5 pionieri attivati (anche gratis in cambio di feedback).
- [ ] 1 articolo tecnico pubblicato.
- [ ] Raccolta sistematica feedback → fix rapidi.

**Giorni 60–90 — Validazione + canale**
- [ ] 10 studi attivi; prime 1–2 referenze scritte.
- [ ] Contatto con **1 distributore/partner non esclusivo** O **1 socio commerciale**.
- [ ] Decisione prezzo definitivo basata su cosa la gente paga davvero.

---

## 6. Se cerchiamo un partner di canale (chi e come)

- **Profilo ideale:** ex-commerciale di TeamSystem/WK in proprio, software house locale che
  serve studi, o commercialista influente con molti colleghi.
- **Offerta:** 30–40% di commissione ricorrente, **non esclusiva**, area/tempo definiti.
- **Alternativa "socio":** chi porta la rete entra con **equity o revenue-share** invece di
  stipendio. "Il 70% di qualcosa che vende batte il 100% di qualcosa che nessuno conosce."

---

## 7. Metriche da guardare (poche, vere)

- N. studi attivi paganti.
- Tasso prova → pagamento.
- Churn mensile (chi disdice).
- CAC (quanto ci costa acquisire un cliente) vs LTV (quanto rende nel tempo).
- N. casi golden pubblici (è anche marketing: "verificato su N casi").

---

## 8. Rischi onesti

- **Senza marketing, il self-serve non parte.** Il prodotto buono non basta: serve farsi
  trovare. Va impostato dal giorno 1, non "dopo".
- **Distributore con esclusiva = trappola.** Evitare.
- **Fiducia:** un nome nuovo nel fisco parte svantaggiato. Si compensa con trasparenza,
  referenze e disclaimer/human-in-the-loop (mai promettere infallibilità).
- **Tempo dei fondatori:** vendere toglie tempo allo sviluppo. Per questo serve, presto,
  o il self-serve automatico o una persona dedicata alla rete.

---

## 9. Vincolo ETS — vendere restando non profit

Siamo un **Ente del Terzo Settore (ETS) non profit**. Vendere software è **attività
commerciale**: per un ETS ha limiti precisi. Decisione presa: **resta attività collaterale
dentro l'ETS** (non si crea una SRL, per ora).

Regole da rispettare (D.Lgs. 117/2017 + DM 107/2021):

1. **Statuto:** deve prevedere le "attività diverse" (vendita software/servizi). Se manca,
   modificarlo **prima** di vendere.
2. **Tetto:** ricavi software **≤ 30% dei ricavi totali** *oppure* **≤ 66% dei costi totali**.
   È il limite che decide se restiamo ETS. Da monitorare ogni trimestre.
3. **Contabilità separata** per l'attività commerciale (obbligatoria).
4. **Tassazione:** il reddito commerciale è tassato (IRES); valutare regimi agevolati ETS.
5. **Utili reinvestiti** nella missione, mai distribuiti.

**Soglia-trigger (da definire ora):** quando i ricavi software si avvicinano al 30% dei
ricavi totali → aprire una **SRL** (anche Impresa Sociale) controllata dall'ETS, prima di
sforare e perdere la qualifica.

> ⚠️ Panoramica per orientarsi, **non** consulenza legale/fiscale. Struttura e regimi vanno
> validati da un **commercialista abilitato** sullo statuto reale e sui numeri attesi.

---

## 10. Canale di partenza: distributore in Sicilia

Si parte dal territorio dove ha sede lo studio. Distributore **ancora da individuare**.

**Profilo da cercare (in ordine di efficacia):**
1. Ex-agente/rivenditore di gestionali (TeamSystem, Zucchetti, WK) ora in proprio — ha già
   i contatti negli studi siciliani.
2. Software house / consulente IT locale che assiste studi di commercialisti.
3. Commercialista influente nell'Ordine (Catania, Palermo, ecc.).

**Dove trovarli:** Ordini dei Dottori Commercialisti siciliani (eventi/PEC), LinkedIn,
gruppi di categoria, passaparola dallo studio.

**Struttura dell'accordo (coerente con l'ETS):**
- Ruolo: procacciatore/rivenditore. **Niente esclusiva nazionale**; al massimo esclusiva
  **regionale a tempo** (es. 12 mesi) con **obiettivi minimi** (decade se non raggiunti).
- Commissione ricorrente **30–40%**.
- **La licenza la emette l'ETS** → i ricavi restano nostri e tracciati nei limiti del §9.
- Proprietà del software e rapporto col cliente **restano nostri**.
- Tutto **per iscritto**: territorio, durata, minimi, IP, condizioni di uscita.

---

## 11. Prossimo passo consigliato

1. **Verifica statuto ETS** (prevede le attività diverse?) con il commercialista + imposta il
   monitoraggio del tetto 30%/66% e la soglia-trigger per la futura SRL.
2. **Sito con prezzo pubblico + prova + pagamento self-serve** e killer-demo: ci rende
   indipendenti da una rete commerciale.
3. **Individuare 1 distributore in Sicilia** (profilo §10), accordo regionale non esclusivo
   a tempo.
