# ia-notebooks

Notebook e progetti di intelligenza artificiale e machine learning, dal didattico al reale: algoritmi implementati da zero in NumPy, pipeline con scikit-learn, dati da database SQL, API e LLM, fino a progetti completi testati.

Autore: Lorenzo Casarosa, docente di informatica, Co-autore di due manuali per la preparazione all'Esame di Maturità, , Data Science and Business Informatics (UNIPI).

## Come è organizzato

Ogni lavoro sta in una cartella numerata (`NN-titolo/`) con un proprio README: obiettivo, livello, fonti, istruzioni per eseguirlo. I notebook sono pubblicati nella versione completa, con soluzioni e output dell'esecuzione.

Ogni lavoro è collocato su uno dei cinque livelli del percorso, descritti in [ROADMAP.md](ROADMAP.md):

| Livello | Nome | Cosa significa |
|---|---|---|
| 1 | Da zero | L'algoritmo implementato a mano con liste o NumPy, per capirne il meccanismo |
| 2 | Librerie | Lo stesso problema con scikit-learn, pipeline e validazione corretta |
| 3 | Dati da database | Dati in SQLite/PostgreSQL, query SQL scritte a mano, risultati riscritti nel database |
| 4 | API e LLM | Modelli serviti con FastAPI, API REST, LLM con output strutturato e tool calling |
| 5 | Progetto completo | Database, modello, API e test automatici in un unico progetto eseguibile |

## Indice

| N. | Titolo | Livello | Stato | Link |
|---|---|---|---|---|
| | Nessun lavoro pubblicato | | | |

## Principi

- Ogni affermazione numerica viene da un'esecuzione reale del codice.
- Metodologia: suddivisione dei dati prima dell'analisi esplorativa, nessun leakage, split temporale quando esiste un asse temporale, seed fissati.
- Le fonti (Géron, *Hands-On Machine Learning*; mlfromscratch; Andrew Ng; documentazione ufficiale delle librerie) sono citate sezione per sezione.
- Nessuna chiave API nel repository: le variabili necessarie sono elencate nei file `.env.example`.

## Come eseguire

I notebook dei livelli 1 e 2 si aprono direttamente su Google Colab (badge nel README di ogni cartella). Per i livelli 3-5, ogni cartella contiene `requirements.txt` e le istruzioni di avvio.
