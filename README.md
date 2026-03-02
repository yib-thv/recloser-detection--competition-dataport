# ⚡ Recloser Fault Detection and Prediction

### DataPort Competition Project

This repository presents an **end-to-end data engineering and machine learning pipeline** for detecting protection events and predicting faults in electrical distribution **reclosers** using operational data collected from Intelligent Electronic Devices (IEDs).

The project integrates **power system protection knowledge**, **data processing**, and **artificial intelligence** techniques to support smarter monitoring of distribution networks.

---

## 📌 Project Motivation

Distribution reclosers are critical protection devices used to isolate faults and maintain service continuity in electrical grids.
Early detection of abnormal behavior enables:

* Reduction of outage duration
* Improved operational reliability
* Preventive maintenance strategies
* Intelligent grid monitoring

This work builds a reproducible pipeline transforming raw SCADA/IED records into predictive models capable of identifying protection events.

---

## ⚙️ End-to-End Pipeline

The proposed workflow includes:

```
IED Raw Files
        ↓
Data acquisition (SCADA / acSELerator)
        ↓
Format-aware ingestion
        ↓
Timestamp reconstruction
        ↓
Chronological ordering
        ↓
Duplicate removal
        ↓
Dataset integration (CSV)
        ↓
Feature engineering
        ↓
Machine Learning Pipeline
```

---

## 📊 Datasets

Two datasets were constructed:

### 🔹 Load Dataset

Contains electrical operational measurements:

* Phase currents (IA, IB, IC)
* Residual current (IG)
* Line voltages (VAB, VBC, VCA)
* Frequency
* Active and reactive power
* Power factor
* Timestamp and anonymized location identifiers

### 🔹 Event Dataset

Contains protection system operations:

* Event type
* Event current
* Protection group
* Reclosing attempt number
* Event timestamp

---

## 🤖 Machine Learning Models

The following models were implemented and evaluated:

* Decision Tree
* Random Forest
* XGBoost
* K-Nearest Neighbors (KNN)
* Long Short-Term Memory (LSTM)

---

## 📈 Evaluation Metrics

Model performance was evaluated using:

* **Accuracy** — overall prediction correctness
* **Precision** — reliability of detected events
* **Recall** — critical metric to minimize false negatives
* **F1-Score** — balance between precision and recall
* **ROC AUC** — discrimination capability between classes

---

## 🧪 Methodology

1. Data acquisition from SEL-351R reclosers
2. Temporal normalization and reconstruction
3. Data cleaning and validation
4. Dataset integration
5. Feature engineering
6. Model training and validation
7. Performance comparison

---

## 📂 Repository Structure

```
recloser-detection--competition-dataport/
│
├── data/              # Processed datasets
├── notebooks/         # Exploratory analysis
├── src/               # Processing and ML scripts
├── figures/           # Pipeline and result figures
├── models/            # Saved trained models
├── requirements.txt
└── README.md
```

---

## 🛠️ Technologies Used

* Python 3.12
* Pandas
* NumPy
* Scikit-learn
* XGBoost
* PyTorch
* Matplotlib
* Jupyter Notebook

---

## 🚀 Installation

Clone the repository:

```bash
git clone https://github.com/yib-thv/recloser-detection--competition-dataport.git
cd recloser-detection--competition-dataport
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## ▶️ Usage

Example training execution:

```bash
python train.py
```

---

## 🔬 Research Context

This project contributes to research areas including:

* Smart Grids
* Power System Protection
* Machine Learning for Energy Systems
* Predictive Maintenance
* Industrial AI

---

## 📈 Results

Models were validated on an independent dataset emphasizing **high recall performance**, ensuring reliable detection of protection events and minimizing missed faults.


---

## 📜 License

MIT License
