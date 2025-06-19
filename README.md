# Progetto del corso di Intelligenza Artificiale e Sicurezza ![License](https://img.shields.io/badge/license-MIT-green.svg)
## Università degli studi di Cagliari - Informatica Applicata e Data Analytics

## Indice
- [Introduzione](#introduzione)
- [Progetto](#progetto)
- [Cartelle](#cartelle)
- [Dataset](#dataset)
- [Installazione](#installazione)

### Introduzione
Il progetto consiste nell'analizzare come l’accuratezza del riconoscimento biometrico tramite EEG (ElettroEncefaloGramma) varia modificando il filtro della banda del segnale (alpha, beta, delta, gamma, theta, broadband).

Le principali **sfide correnti** nell'ambito dell'EEG come riconoscimento biometrico sono l'utilizzo e l'applicazione in contesti realistici, e la riduzione del numero di elettrodi utilizzati.

### Progetto
Si effettua il preprocessing dei dati e divisione per bande di frequenza, successivamente si effettuano una serie di analisi:
- Ricerca della banda di frequenza maggiormente discriminante;
- Verifica della banda di frequenza alfa come discriminante nella rilevazione REC (eyes closed) rispetto la rilevazione REO (eyes open);
- Proposta di nuove bande di frequenza;
- Confronto tra modelli shallow e deep learning;
- Riduzione dei canali.
All'interno del notebook è possibile approfondire ognuno di questi aspetti.

### Cartelle
- **confusion_matrix:** Cartella contenente le varie matrici di confusione prodotte, divise per task e modello.
- **dataset:** Cartella contenente i sub-dataset utilizzati.
- **img:** Cartella contenente le immagini contenute nel notebook.
- **tuning:** Cartella contenente i risultati del tuning.

### Dataset
Il Dataset EEG Motor Movement/Imagery, acquisito presso il [Wadsworth Center, New York State Department of Health](https://pubmed.ncbi.nlm.nih.gov/15188875/) tramite [BCI 2000 (Brain-Computer Interface)](https://www.bci2000.org/mediawiki/index.php/Main_Page), è stato creato per lo sviluppo di sistemi di interfaccia cervello-computer che permettano alle persone di controllare dispositivi esterni attraverso l'attività cerebrale.

### Installazione
Si clona la repository del progetto e ci si sposta nella cartella:
```bash
git clone https://github.com/ChiccoSechi/EEG-recognition.git
cd path/EEG-recognition
```

Successivamente si installano le librerie necessarie dal file `requirements.txt`:

```bash
pip install -r requirements.txt
```

Verranno installate le seguenti librerie, se non presenti:
- mne
- seaborn
- scikit-learn
- tensorflow
- keras-tuner
- gdown
- tqdm
- notebook
- pandas

Infine è possibile aprire il file `.ipynb` come si preferisce.