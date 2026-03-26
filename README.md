🩺 Predizione del Diabete - Tesi di Laurea Triennale

Questo repository contiene il notebook e il codice sviluppato per il mio progetto di Tesi di Laurea Triennale. L'obiettivo dello studio è l'analisi di dati clinici e l'addestramento di diversi modelli di Machine Learning per prevedere l'insorgenza del diabete nei pazienti.

📊 Il Dataset

Il progetto si basa sul dataset diabetes_prediction_dataset.csv, composto da 100.000 record. Il dataset combina dati demografici, storici e misurazioni cliniche.

Le feature principali includono:

    Dati Demografici: gender (Genere), age (Età).

    Storia Clinica e Stile di vita: hypertension (Ipertensione), heart_disease (Patologie cardiache), smoking_history (Storico di fumo).

    Misurazioni Mediche: bmi (Indice di Massa Corporea), HbA1c_level (Livello di Emoglobina Glicata), blood_glucose_level (Glucosio nel sangue).

    Target: diabetes (Variabile binaria: 0 = Negativo, 1 = Positivo).

🛠️ Pipeline e Metodologia

All'interno del notebook Lavoro_Tesi.ipynb ho sviluppato un'intera pipeline di Data Science, affrontando le seguenti fasi:

    Analisi Esplorativa (EDA) e Pulizia Dati:

        Ricerca e gestione dei missing values.

        Identificazione ed eliminazione dei record duplicati.

        Visualizzazione della distribuzione delle classi (es. bilanciamento per genere e target) usando Matplotlib e Seaborn.

    Data Preprocessing:

        Normalizzazione e scalatura dei dati continui utilizzando MinMaxScaler e RobustScaler.

        Encoding delle variabili categoriche tramite OneHotEncoder.

        Analisi di multicollinearità (VIF - Variance Inflation Factor).

    Gestione dello Sbilanciamento delle Classi:
    Essendo un tipico caso di rilevamento di patologie, il dataset presenta un forte sbilanciamento. Ho sperimentato diverse tecniche della libreria imbalanced-learn:

        Over-sampling: RandomOverSampler, SMOTE, BorderlineSMOTE.

        Under-sampling: RandomUnderSampler, EditedNearestNeighbours (ENN), TomekLinks.

        Tecniche Ibride: SMOTETomek.

    Addestramento dei Modelli:
    Sono stati testati ed esaminati i seguenti algoritmi di classificazione:

        Logistic Regression

        K-Nearest Neighbors (KNN)

        Support Vector Classifier (SVC)

        Random Forest Classifier

📈 Valutazione dei Risultati

In ambito medico, ridurre i Falsi Negativi (classificare come "sano" un paziente effettivamente malato) è di fondamentale importanza. Nel progetto, la valutazione dei modelli è stata eseguita non solo sull'accuracy generale, ma dando forte priorità alle metriche di richiamo (Recall) e all'analisi della matrice di confusione. Le performance sono state riepilogate e ordinate proprio in base alle percentuali di falsi negativi generati.
💻 Stack Tecnologico

    Linguaggio: Python

    Gestione Dati: Pandas, NumPy

    Machine Learning: Scikit-Learn

    Balancing: Imbalanced-Learn (imblearn)

    Data Visualization: Matplotlib, Seaborn

🚀 Come visualizzare il progetto

    Clona il repository:
    Bash

    git clone https://github.com/TuoUsername/TuoRepoDiabete.git

    Installa le dipendenze richieste:
    Bash

    pip install pandas numpy scikit-learn imbalanced-learn matplotlib seaborn tabulate

    Avvia il notebook tramite Jupyter:
    Bash

    jupyter notebook Lavoro_Tesi.ipynb
