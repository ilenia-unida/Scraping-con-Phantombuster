# 👻 Flusso Automatico: Integrazione PhantomBuster e AI (Gemini)

Un workflow avanzato, costruito con **n8n**, che dimostra l'integrazione fluida tra un servizio di scraping esterno (PhantomBuster) e l'Intelligenza Artificiale (Google Gemini). Questo flusso è progettato per recuperare i risultati di un PhantomBuster Agent, pulirli, analizzarli e archiviarli in modo strutturato.

## ✨ Caratteristiche & Funzionalità

* **Integrazione PhantomBuster:** 👻 Recupera automaticamente i risultati di un Agent di PhantomBuster già eseguito (es. uno scraper di LinkedIn o di Google Search).
* **AI Data Extraction:** 🧠 Utilizza un **AI Agent** con il modello **Google Gemini** per analizzare il testo non strutturato e identificare, estrarre e normalizzare dati chiave (ad esempio, Nome e Indirizzo Email).
* **Gestione del Volume:** Limita il numero di elementi elaborati in una singola esecuzione (nodo **Limit**) per ottimizzare i costi e la gestione dei dati.
* **Archiviazione finale:** 📊 Salva i dati finali puliti e strutturati in una tabella Airtable.

## 🚀 Struttura del Flusso

Il flusso è composto dai seguenti nodi:

1.  **Schedule Trigger:** 🕒 Avvia l'esecuzione del flusso all'orario desiderato.
2.  **Edit Fields:** Imposta variabili o parametri di ricerca (anche se in questo caso l'output è statico).
3.  **Get the output of an agent (PhantomBuster):** 📥 Nodo chiave che recupera i risultati del PhantomBuster Agent.
4.  **Limit:** 🛑 Limita il numero di elementi da processare (es. 10 record).
5.  **Clean & Format (Code):** 🧹 Pulisce i dati grezzi ricevuti, rendendoli leggibili.
6.  **AI Agent (Gemini):** 💡 Analizza il testo e restituisce il JSON strutturato.
7.  **Pulire l’output (Code):** 🛠️ Pulisce l'output del JSON generato dall'AI.
8.  **Create a record (Airtable):** 💾 Salva i dati finali.

## 📺 Video di Spiegazione

Per una spiegazione dettagliata del funzionamento, della logica e della configurazione dei nodi, guarda il video qui sotto:

[Spiegazione dettagliata del flusso PhantomBuster e AI su YouTube](https://youtu.be/rGYWzIco6gw)

## 🛠️ Requisiti

Per poter utilizzare questo flusso, dovrai configurare le seguenti credenziali nel tuo ambiente n8n:

* **PhantomBuster API Account**
* **Google Gemini (PaLM) API Account**
* **Airtable Personal Access Token Account**

---

