---
titolo: "3 Weekend fuori dalla Comfort Zone: L'illusione dell'AI e il bivio Cloud Architect"
data: "Luglio 2026"
tags: ["DataEngineering", "VPS", "Docker", "DevOps", "ContinuousLearning", "AI"]
grafico:
  tipo: "pie"
  etichette: ["Data Eng. & SEC", "CI/CD & Docker", "PostgreSQL & Views", "API Resiliency", "Testing & Logging"]
  dati: [30, 25, 20, 15, 10]
  labelLegenda: "Ripartizione tempo (%)"
---

Nell'ultimo anno mi sono diviso tra il ruolo di Scrum Master e lo sviluppo RPA, muovendomi spesso nel mondo dei dati 'a valle' con Denodo e PowerBI. Ebbene tre weekend fa ho deciso di accettare una sfida diversa. Un amico si era incagliato usando Claude su un modello finanziario e ho colto il pretesto per sviluppare CASHEN: una serie di container Docker su una VPS economica gestiti tramite crontab per fare analisi tecnica e inviare un report settimanale su un gruppo Telegram.

Intendiamoci: nulla di trascendentale o cloud-native. Ma nel 2026, usare una VPS da 3,66€ IVA inclusa ha un senso preciso: ti costringe a gestire RAM e CPU al milligrammo, affrontando logiche di Azure DevOps (pipeline, library, gestione dei secret) e Docker da zero. 

Guardando la frammentazione del tempo speso, lo sforzo reale ha tradito le aspettative iniziali:

* **30% - Data Engineering & XBRL SEC (Python):** Gestione del parsing dei dati finanziari da EDGAR, distinguendo i report 10-Q dai 10-K per evitare il look-ahead bias.
* **25% - CI/CD (Azure Pipelines) & Docker:** Configurazione del deploy e isolamento degli scraper in container indipendenti su rete condivisa.
* **20% - Database (PostgreSQL, Views, SQL):** Uso del DB come motore logico con l'architettura degli schemi grezzi e dello schema *silver*.
* **15% - API Resiliency & Rate Limiting:** Gestione difensiva dei tier gratuiti tramite code database-driven.
* **10% - Testing, Logging & Observability:** Tracciabilità del flusso e reportistica vettoriale.

### L'illusione dell'AI: Percezione, Conoscenza, Esperienza
Sviluppando questo progetto e usando l'AI in maniera massiva (attraverso tool come *antigravity* dotati di skill, MCP e hooks), ho vissuto tre passaggi cognitivi accelerati:

1. **La Percezione:** L'illusione iniziale. L'AI ti spiega un argomento in modo così semplice che pensi di averlo interiorizzato. Poi vieni interpellato singolarmente e cadi dal pero letteralmente.
2. **La Conoscenza:** Il livello successivo, figlio dell'esposizione. Impari a lanciare un `docker ps -a` o a debuggare al volo gli errori più frequenti.
3. **L'Esperienza:** La sensibilità umana di chi si è fatto male. Quella che ti fa prevenire le dinamiche in sicurezza per evitarti commit fatti a caso (al quarto commit fallito di fila sulla pipeline YAML, ho scritto nei log: *'too many commits make Vit sad'*).

Questo è il vero punto di partenza per capire come cambierà il nostro lavoro. Spesso quando si parla di AI si invoca il metodo HITL (Human-in-the-Loop), pretendendo dall'uomo un livello di etica e controllo impareggiabile. Ma come può l'uomo fare da loop se è inesperto e si ritrova a essere un collo di bottiglia per bande di informazioni esageratamente dense?

Se accetti i tuoi limiti di banda sei lento; se vuoi essere sicuro hai bisogno di un'esperienza che oggi ancora non hai. Se manca un metodo discusso intimamente con se stessi, vince a mani basse la logica del **'doganiere di second'ordine'**: quello che fa passare tutto con un sorriso, nella speranza che non ci sia codice malevolo o fallato. Questo approccio uccide le aziende ed è difficilissimo da scovare. Servono nuovi sistemi per aiutare l'uomo in questo viaggio quantico che l'AI ci pone davanti.

### Il Bivio Futuro: Quali prossimi passi?
Al netto delle considerazioni filosofiche, le scelte di oggi pesano esponenzialmente sul nostro lavoro di domani. Questo viaggio nelle tubature del codice mi ha messo davanti a due strade chiare per la mia specializzazione attraverso l'ecosistema Google Cloud:

* **Data Cloud Architect:** Per unire il mio background sui dati (Denodo, PowerBI) alle logiche di ingestion, pulizia e strutturazione del dato su larga scala nel cloud, cavalcando quel 50% di tempo speso tra Data Engineering e Database.
* **Cloud Architect:** Per focalizzarmi interamente sulla progettazione di infrastrutture robuste, sicure e disaccoppiate, stimolato da quel 50% di tempo speso a lottare con Docker, reti, CI/CD e limiti hardware.

Tre weekend non cambiano una carriera, ma mi hanno ricordato che per governare l'AI di domani, dobbiamo smettere di fare i doganieri e ricominciare a fare esperienza.
