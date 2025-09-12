# Kreditrisiko-Bewertung-mit-Machine-Learning
Im Rahmen des Projekts wurde eine Machine-Learning-Pipeline zur Vorhersage der Kreditwürdigkeit auf Basis des German Credit Dataset entwickelt. Sie umfasst Datenaufbereitung, Modelltraining, Explainable AI, Bereitstellung via REST-API und Visualisierung im Dashboard – von Analyse bis Produktion.
Hauptfunktionen
📊 Explorative Datenanalyse (EDA)

Visualisierungen zur Klassenverteilung, Merkmalverteilungen und Korrelationen.
Einblicke in demografische Daten von Kreditnehmern und Kreditmerkmale.

⚙️ Datenvorverarbeitung

One-Hot-Encoding für kategoriale Variablen.
Skalierung und Merkmalsauswahl mit StandardScaler und SelectKBest.

🧠 Machine-Learning-Modelle

Logistische Regression, Entscheidungsbäume, Random Forests, Gradient Boosting, SVM.

Hyperparameter-Tuning mit GridSearchCV.
Modellvergleich anhand von Genauigkeit, Konfusionsmatrix und Klassifikationsberichten.

🔍 Modellinterpretierbarkeit

Feature-Importance-Plots für Random Forests.
SHAP (SHapley Additive exPlanations) für globale und lokale Modellerklärungen.

💾 Modell-Speicherung

Speichern trainierter Modelle, Skalierer, Selektoren und Feature-Sets mit joblib.

🌐 Bereitstellung

Flask-API für Echtzeit-Kreditrisikovorhersagen (/predict-Endpoint).
Streamlit-Dashboard für interaktive Vorhersagen ohne Programmierkenntnisse.

📂 Projektstruktur

Separate Skripte für Training, Visualisierung, API-Hosting und Tests.
Assets-Ordner mit allen generierten Diagrammen zur Dokumentation.
Technologie-Stack
Python: Zentrale Programmiersprache für Datenverarbeitung und Modellierung.

Bibliotheken:
pandas, numpy, matplotlib, scikit-learn, shap, flask, streamlit

Bereitstellung: Flask REST API, Streamlit Benutzeroberfläche.
pandas, numpy, matplotlib, scikit-learn, shap, flask, streamlit

Bereitstellung: Flask REST API, Streamlit Benutzeroberfläche.

---

## 📊 Visualisierungen

### 1. Klassenverteilung
Zeigt die Balance zwischen guten und schlechten Krediten.

![Class Balance](assets/01_class_balance.png)

---

### 2. Verteilungen wichtiger Merkmale

**Kreditbetrag**
![Credit Amount](assets/02_Credit_amount_hist.png)

**Alter**
![Age Distribution](assets/02_Age_in_years_hist.png)

**Laufzeit in Monaten**
![Duration](assets/02_Duration_in_month_hist.png)

---

### 3. Korrelationen
Korrelation zwischen numerischen Merkmalen:

![Correlation Heatmap](assets/03_correlation_heatmap.png)

---

### 4. Feature Importances (Random Forest)
Wichtige Einflussgrößen für die Kreditrisikovorhersage:

*(erst nach Modelltraining verfügbar)*

![Feature Importances](assets/04_feature_importances_rf.png)

---

### 5. SHAP-Analysen
Globale und lokale Erklärbarkeit des Random-Forest-Modells:

- **Globale Wichtigkeit (Balkendiagramm)**
![SHAP Bar](assets/05_shap_summary_bar.png)

- **Verteilung (Beeswarm)**
![SHAP Beeswarm](assets/06_shap_beeswarm.png)

---

## ⚙️ Technologien

- **Python 3.11**
- **Bibliotheken**:  
  `pandas`, `numpy`, `matplotlib`, `scikit-learn`, `shap`, `flask`, `streamlit`, `joblib`

---

## 🌐 Nutzung

### 1️⃣ Training & Speichern des Modells
```bash
python train_and_save_model.py

### 2️⃣ API starten
python Credit\ Risk\ Api.py

### 3️⃣ API testen
python test_api.py

📌 Anwendungsfall

Dieses System kann Banken und Kreditinstituten helfen, Kreditrisiken automatisch einzuschätzen und so bessere Entscheidungen bei der Kreditvergabe zu treffen.
Die Kombination aus präzisen ML-Modellen und Interpretierbarkeit (SHAP) ermöglicht nachvollziehbare und faire Entscheidungen.

