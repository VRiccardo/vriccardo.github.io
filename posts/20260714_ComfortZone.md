---
titolo: "3 Weekend fuori dalla Comfort Zone: L'illusione dell'AI e il bivio Cloud Architect"
data: "Luglio 2026"
tags: ["DataEngineering", "VPS", "Docker"]
grafico:
  tipo: "pie"
  etichette: ["Data Eng. & SEC", "CI/CD & Docker", "PostgreSQL & Views", "API Resiliency", "Testing & Logging"]
  dati: [30, 25, 20, 15, 10]
  labelLegenda: "Ripartizione tempo (%)"
---

Tre weekend fa ho deciso di accettare una sfida. Un amico si era incagliato usando Claude su un suo modello finanziario personale e ho colto il pretesto per sviluppare CASHEN: una serie di container Docker su una VPS economica gestiti tramite crontab per fare analisi e inviare un report settimanale su una chat personale.

Intendiamoci: nulla di trascendentale o cloud-native. Ma nel 2026, usare una VPS da 3,66€ IVA inclusa ha un senso preciso: ti costringe a gestire RAM e CPU al milligrammo, affrontando logiche di Azure DevOps (pipeline, library, gestione dei secret) e Docker da zero. 

Guardando la frammentazione del tempo speso, lo sforzo reale ha tradito le mie aspettative iniziali (storicamente sempre troppo rosee):

* **30% - Data Engineering & XBRL SEC (Python):** Gestione del parsing dei dati finanziari da EDGAR, distinguendo i report 10-Q dai 10-K per evitare il look-ahead bias, oppure ticker che subiscono un cambio codice (es. Alphabet ha cambiato ticker più volte: GOOG, GOOGL, etc)
* **25% - CI/CD (Azure Pipelines) & Docker:** Configurazione del deploy e isolamento degli scraper in container indipendenti su rete condivisa. (Ho provato Azure Pipelines: dall'installazione dell'Agent su VPS alla configurazione della pipeline, fino alla gestione di secret e variabili).
* **20% - Database (PostgreSQL, Views, SQL):** Uso del DB come motore logico con l'architettura degli schemi grezzi (1 schema per singolo provider di dati) e delle viste in **silver** e **gold** per raffinare il dato.
* **15% - API Resiliency & Rate Limiting:** Gestione difensiva dei tier gratuiti tramite code database-driven (se mandi troppe chiamate hai error 429, oppure alcuni provider gestiscono una sorta di wallet con crediti free che si rinnova giornalmente e non sempre hai rapporto 1 chiamata api per 1 credito).
* **10% - Testing, Logging & Observability:** Tracciabilità del flusso e reportistica vettoriale (OpenTelemetry, gestione puntamenti log/span/metrica + Dozzle per avere una semplice dashboard sotto mano).

### L'illusione dell'AI: Percezione, Conoscenza, Esperienza
Sviluppando questo progetto e usando l'AI in maniera massiva (attraverso tool come *antigravity* dotati di skill, MCP e hooks), ho vissuto tre passaggi cognitivi accelerati:

1. **La Percezione:** L'illusione iniziale. L'AI ti spiega un argomento in modo così semplice che pensi di averlo interiorizzato. Poi vieni interpellato singolarmente e cadi dal pero letteralmente.
2. **La Conoscenza:** Il livello successivo, figlio dell'esposizione. Impari a usare Docker dalla versione più banale di un `docker ps -a`, fino a debuggare al volo gli errori più frequenti (spesso dettati dall'inesperienza o fretta).
3. **L'Esperienza:** La sensibilità umana di chi si è fatto male. Quella che ti fa prevenire le dinamiche in sicurezza per evitarti commit fatti a caso (al quarto commit correttivo di fila sulla pipeline YAML, ho scritto nei log: *'too many commits make Vit sad'*).

Questo è il vero punto di partenza per capire come cambierà il nostro lavoro. Spesso quando si parla di AI si invoca il metodo HITL (Human-in-the-Loop), pretendendo dall'uomo un livello di etica e controllo impareggiabile. Ma come può l'uomo fare da loop se è inesperto? Rischia di ritrovarsi lui stesso collo di bottiglia, schiacciato da un flusso di informazioni troppo denso per essere processato in sicurezza.

Se accetti i tuoi limiti di banda sei lento; se vuoi essere sicuro hai bisogno di un'esperienza che oggi ancora non hai. Se manca un metodo discusso intimamente con sé stessi, vince a mani basse la logica del **'doganiere di second'ordine'**: quello che fa passare tutto con un sorriso, nella speranza che non ci sia codice malevolo o fallato. Questo approccio uccide le aziende ed è difficilissimo da scovare. Servono nuovi sistemi per aiutare l'uomo in questo viaggio quantico che l'AI ci pone davanti.

### Il Bivio Futuro: Quali prossimi passi?
Al netto delle considerazioni filosofiche, oggi più di prima le scelte che facciamo pesano esponenzialmente sul nostro lavoro di domani. Con questo viaggio nelle tubature del codice mi ritrovo davanti a due possibili strade per la mia specializzazione futura all'interno dell'ecosistema Big G:

* **Data Cloud Architect:** Per unire il mio background sui dati (Denodo, PowerBI) alle logiche di ingestion, pulizia e strutturazione del dato su larga scala nel cloud, cavalcando quel 50% di tempo speso tra Data Engineering e Database.
* **Cloud Architect:** Per focalizzarmi interamente sulla progettazione di infrastrutture robuste, sicure e disaccoppiate, stimolato da quel 50% di tempo speso a lottare con Docker, reti, CI/CD e limiti hardware.

Tre weekend non regalano proiettili d'argento, ma hanno avuto il potere di ricordarmi che per governare l'AI di domani, dobbiamo smettere di fare i doganieri e ricominciare a fare esperienza, tanta esperienza.