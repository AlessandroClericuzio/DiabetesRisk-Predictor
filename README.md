# 🩺 DiaDetect-ML: Predizione del Diabete (Tesi Triennale)

Questo repository contiene il notebook e il codice sviluppato per il mio progetto di Tesi di Laurea Triennale. L'obiettivo dello studio è l'analisi di dati clinici e l'addestramento di diversi modelli di Machine Learning per prevedere l'insorgenza del diabete nei pazienti.

---

## 📊 Il Dataset

I dati utilizzati per addestrare e testare i modelli provengono da un dataset pubblico disponibile su **Kaggle**: 
🔗 **[Diabetes Prediction Dataset](https://www.kaggle.com/datasets/iammustafatz/diabetes-prediction-dataset)** *(inserisci qui il link esatto se hai usato una versione diversa)*.

Il dataset è composto da 100.000 record e combina dati demografici, storici e misurazioni cliniche. Le feature principali includono:
* **Dati Demografici:** `gender` (Genere), `age` (Età).
* **Storia Clinica e Stile di vita:** `hypertension` (Ipertensione), `heart_disease` (Patologie cardiache), `smoking_history` (Storico di fumo).
* **Misurazioni Mediche:** `bmi` (Indice di Massa Corporea), `HbA1c_level` (Livello di Emoglobina Glicata), `blood_glucose_level` (Glucosio nel sangue).
* **Target:** `diabetes` (Variabile binaria: 0 = Negativo, 1 = Positivo).

---

## 🛠️ Pipeline e Metodologia

All'interno del notebook `Lavoro_Tesi.ipynb` ho sviluppato un'intera pipeline di Data Science, affrontando le seguenti fasi:

1. **Analisi Esplorativa (EDA) e Pulizia Dati:**
   * Ricerca e gestione dei missing values.
   * Identificazione ed eliminazione dei record duplicati.
   * Visualizzazione della distribuzione delle classi usando `Matplotlib` e `Seaborn`.

2. **Data Preprocessing:**
   * Normalizzazione e scalatura dei dati continui utilizzando `MinMaxScaler` e `RobustScaler`.
   * Encoding delle variabili categoriche tramite `OneHotEncoder`.

3. **Gestione dello Sbilanciamento delle Classi:**
   Essendo un tipico caso di rilevamento di patologie, il dataset presenta un forte sbilanciamento. Ho sperimentato diverse tecniche della libreria `imbalanced-learn`:
   * **Over-sampling:** RandomOverSampler, SMOTE, BorderlineSMOTE.
   * **Under-sampling:** RandomUnderSampler, EditedNearestNeighbours (ENN), TomekLinks.
   * **Tecniche Ibride:** SMOTETomek.

4. **Addestramento dei Modelli:**
   Sono stati testati ed esaminati i seguenti algoritmi di classificazione:
   * Logistic Regression
   * K-Nearest Neighbors (KNN)
   * Support Vector Classifier (SVC)
   * Random Forest Classifier

---

## 📈 Valutazione dei Risultati

In ambito medico, ridurre i **Falsi Negativi** (classificare come "sano" un paziente effettivamente malato) è di fondamentale importanza. Nel progetto, la valutazione dei modelli è stata eseguita dando forte priorità alle metriche di richiamo (Recall) e all'analisi della matrice di confusione. Le performance sono state riepilogate e ordinate proprio in base alle percentuali di falsi negativi generati per individuare il modello più sicuro dal punto di vista clinico.

---

## 💻 Stack Tecnologico

* **Linguaggio:** Python
* **Gestione Dati:** Pandas, NumPy
* **Machine Learning:** Scikit-Learn
* **Balancing:** Imbalanced-Learn (imblearn)
* **Data Visualization:** Matplotlib, Seaborn

---

## 🚀 Come visualizzare il progetto

1. Clona il repository:
   ```bash
   git clone [https://github.com/TuoUsername/TuoRepoDiabete.git](https://github.com/TuoUsername/TuoRepoDiabete.git)

2. Installa le dipendenze richieste:
  ```bash
   pip install pandas numpy scikit-learn imbalanced-learn matplotlib seaborn tabul
  ```
2. Scarica il dataset da Kaggle e inseriscilo nella cartella principale del progetto.

3. Avvia il notebook tramite Jupyter:
   ```bash
   jupyter notebook Lavoro_Tesi.ipynb
   
