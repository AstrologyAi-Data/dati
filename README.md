# Dati di nascita anonimi per test astrologici

Dati usati nei repo **statistiche** e **machine-learning**. Solo ricerca non commerciale.

**Niente nomi**: ogni persona è un codice casuale. La data di nascita resta, perché serve all'analisi, ma non
c'è nessun modo diretto di risalire alla persona. Le diagnosi o le cause di morte non sono collegate a nomi.

| Cartella | Contenuto | Fonte |
|---|---|---|
| `wikidata/wikidata_gruppi.json` | gruppi (suicidio, depressione, bipolare, overdose…): codice casuale, data di nascita al giorno, longitudine a 0,1° | [Wikidata](https://www.wikidata.org) (CC0) e Wikipedia |
| `wikidata/contesto.json` | controlli famosi e contesto (paese, mestiere, sesso, fama, patrimonio, titolo, università) con gli stessi codici | Wikidata |
| `astroseek/astroseek_anonimo.csv` | data, ora, posizioni dei pianeti e case, voto di affidabilità; senza nome né professione | [Astro-Seek](https://www.astro-seek.com) |
| `gauquelin/gauquelin_anonimo.csv` | professione, data, ora, luogo; senza nomi né identificatori | [CURA](https://cura.free.fr), [opengauquelin](https://github.com/tig12/g5) |

## Non inclusi

- **Astro-Databank**: l'export ha un avviso di Astrodienst. La sezione `research_data` (categorie, relazioni, eventi)
  può essere usata per ricerca, ma la **pubblicazione richiede il permesso del titolare**. Nei repo ci sono solo i
  risultati aggregati. Per rifare l'analisi serve richiedere l'export ad Astrodienst.
- Nomi delle persone e collegamento tra nome e diagnosi.

## Note

- Date di Wikidata: precisione al giorno, dal 1800, calendario gregoriano. Il 1° gennaio è spesso una data
  "segnaposto" e nelle analisi va escluso.
- I gruppi "(testo)" e "(lingue)" sono indiretti: la frase compare nella biografia, ma potrebbe riguardare altri.
- Per rigenerare i file da Wikidata: `analisi/scarica_wikidata.py`, `scarica_indiretti.py` e `scarica_contesto.py`
  nel repo **statistiche**.
