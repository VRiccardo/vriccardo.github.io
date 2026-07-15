# Ciao Vit! - Personal Blog & Timeline

Un blog statico personale ospitato su GitHub Pages. La pagina principale carica dinamicamente articoli scritti in formato Markdown, supportando front-matter YAML per i metadati, grafici Chart.js interattivi e layout ottimizzati per dispositivi mobili.

## Struttura del Progetto

La struttura dei file all'interno del repository è la seguente:

```
├── .nojekyll            # Disattiva l'elaborazione Jekyll su GitHub Pages (permette di servire i file raw .md)
├── README.md            # Questa documentazione
├── index.html           # Pagina principale (Single Page Application statica)
├── posts.json           # Registro in formato JSON degli articoli attivi da caricare
└── posts/               # Cartella contenente i singoli articoli in formato Markdown (.md)
    ├── 20260714_ComfortZone.md
    └── 20260710_HelloWorld.md
```

## Come Aggiungere un Nuovo Articolo

Per pubblicare un nuovo articolo sul blog, segui questi passaggi:

1. **Crea il file Markdown**: all'interno della cartella `posts/`, crea un file con estensione `.md` (es. `posts/20260715_MioPost.md`).
2. **Definisci i Metadati (Front-Matter)**: all'inizio del file, inserisci le informazioni dell'articolo racchiuse tra tre trattini `---`:
   ```yaml
   ---
   titolo: "Il mio nuovo articolo"
   data: "Luglio 2026"
   tags: ["AI", "GCP", "DevOps"]
   # (Opzionale) Aggiungi un grafico interattivo
   grafico:
     tipo: "pie" # "pie", "bar", "line", etc.
     etichette: ["Categoria A", "Categoria B"]
     dati: [70, 30]
     labelLegenda: "Distribuzione (%)"
   ---
   Inserisci qui il testo dell'articolo in formato Markdown standard...
   ```
3. **Registra l'articolo**: apri il file `posts.json` nella root del progetto e aggiungi il percorso relativo del nuovo file creato all'array:
   ```json
   [
     "posts/20260714_ComfortZone.md",
     "posts/20260710_HelloWorld.md",
     "posts/20260715_MioPost.md"
   ]
   ```
4. **Fai il Commit e Push**: invia le modifiche a GitHub. L'articolo apparirà automaticamente sulla timeline!

---

## Caratteristiche Principali del Sito

- **Parsing in-Browser**: Gli articoli in Markdown con front-matter YAML vengono scaricati dinamicamente ed elaborati lato client tramite `js-yaml` e `marked.js` senza necessità di compilazione locale o backend.
- **Grafici Integrati**: Utilizza `Chart.js` per visualizzare grafici personalizzati direttamente all'interno degli articoli semplicemente configurandoli nei metadati.
- **Ottimizzato per Mobile**: Il layout si adatta automaticamente per garantire massima leggibilità anche su piccoli schermi (rimozione linee timeline, ridimensionamento font e grafici).
- **Lettura ad Espansione**: Gli articoli più lunghi di 200px vengono mostrati inizialmente in un riquadro compatto con una sfumatura sul fondo e possono essere espansi o ridotti con una transizione fluida.
