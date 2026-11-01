# Roadmap

Percorso dal didattico al reale in cinque livelli. Le voci si spuntano quando il lavoro corrispondente è pubblicato; ogni voce rimanda alla sua cartella.

## Livello 1. Da zero

Algoritmi implementati con liste o NumPy, senza librerie di machine learning.

- [x] NumPy: dalle liste Python agli array vettorizzati → [01-knn-from-scratch-numpy](01-knn-from-scratch-numpy/) (parte A)
- [x] k-Nearest Neighbors → [01-knn-from-scratch-numpy](01-knn-from-scratch-numpy/) (parte B)
- [ ] Regressione lineare con discesa del gradiente
- [ ] Rete neurale con backpropagation
- [ ] Alberi di decisione

## Livello 2. Librerie

Gli stessi problemi con scikit-learn, con attenzione alla validazione.

- [ ] Pipeline, preprocessing e cross-validation
- [ ] Random forest e importanza delle feature
- [ ] Progetto end-to-end sui prezzi delle case (stile Géron, cap. 2)
- [ ] Serie temporali: split temporale e valutazione corretta

## Livello 3. Dati da database

I dati vivono in un database progettato; il modello li legge e vi riscrive i risultati.

- [ ] Schema SQLite, caricamento dei dati e query di controllo qualità
- [ ] Feature costruite in SQL e lette con `pandas.read_sql`
- [ ] Predizioni salvate nel database e interrogate con SQL
- [ ] Migrazione a PostgreSQL

## Livello 4. API e LLM

Il modello esce dal notebook.

- [ ] Consumare un'API REST esterna come sorgente di dati
- [ ] Servire un modello con FastAPI e validazione Pydantic
- [ ] Chiamare un LLM via API con output JSON strutturato
- [ ] Tool calling: il modello chiede di eseguire funzioni Python
- [ ] Ciclo agentico scritto a mano, senza framework
- [ ] RAG di base su documenti propri

## Livello 5. Progetti completi

Database, modello, API e test automatici in un unico progetto eseguibile.

- [ ] Primo progetto completo: da definire

## Prossimi passi

- Regressione lineare con discesa del gradiente (livello 1), con confronto con `LinearRegression` di scikit-learn.
