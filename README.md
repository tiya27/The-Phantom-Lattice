# The Phantom Lattice

---

# Overview

This repository contains our implementation of **Problem Statement 2** from the **QMP26 Case Study**:

> The Phantom Lattice

The project focuses on detecting anomalous market behavior using high-frequency synthetic trading data.

We build a streaming anomaly-detection pipeline inspired by real-world quantitative trading surveillance systems and market microstructure analytics.

Core components include:

* rolling feature engineering
* volatility regime detection
* streaming PCA
* anomaly scoring
* reconstruction-error monitoring
* market-state classification
* kill-switch simulation
* walk-forward robustness analysis

The implementation combines statistical learning, signal processing, and quantitative risk-monitoring techniques commonly used in high-frequency trading systems.

---

# Problem Statement

We analyze synthetic tick-level market data to identify unstable or anomalous trading regimes in real time.

The objective is to build a lightweight monitoring framework capable of:

* identifying structural shifts
* detecting abnormal volatility bursts
* recognizing hidden latent market states
* triggering defensive kill-switch mechanisms during instability

The system is evaluated using partially labeled anomaly data.

---

# Dataset

The repository uses synthetic tick-level datasets provided in the case study.

## Files Used

```text
ticks_mon.csv
ticks_tue.csv
ticks_wed.csv
ticks_thu.csv
labels_wed.csv
```

---

# Repository Structure

```text
.
├── notebook/
│   └── Team_2.ipynb
│
├── data/
│   ├── ticks_mon.csv
│   ├── ticks_tue.csv
│   ├── ticks_wed.csv
│   ├── ticks_thu.csv
│   └── labels_wed.csv
│
├── src/
│   ├── feature_engineering.py
│   ├── anomaly_detection.py
│   ├── streaming_pca.py
│   ├── volatility_analysis.py
│   ├── regime_detection.py
│   ├── kill_switch.py
│   └── utils.py
│
└── plots/
```

---

# Features

## Part 1 — Feature Engineering & Market Statistics

* Tick-level return computation
* Rolling volatility estimation
* Spread and liquidity analysis
* Time-window aggregation
* Market microstructure statistics

---

## Part 2 — Streaming PCA & Latent Structure

* Online dimensionality reduction
* Dynamic covariance analysis
* Principal component tracking
* Latent factor monitoring
* Regime drift visualization

---

## Part 3 — Anomaly Detection Framework

* Reconstruction-error scoring
* Statistical thresholding
* Rolling z-score analysis
* Outlier regime detection
* Event clustering and labeling

---

## Part 4 — Kill-Switch & Regime Monitoring

* Real-time instability scoring
* Trigger threshold design
* Regime-shift identification
* Emergency shutdown simulation
* Walk-forward robustness analysis

---

## Bonus — Advanced Extensions

* Adaptive thresholds
* Streaming model improvements
* Alternative anomaly metrics
* Hidden-state analysis
* Real-time monitoring enhancements

---

# Key Visualizations

## Rolling Volatility

---

## Streaming PCA Components

---

## Anomaly Score Timeline

---

## Regime Shift Detection

---

# Installation

Clone the repository:

```bash
git clone https://github.com/tiya27/The-Phantom-Lattice
cd The-Phantom-Lattice
```

Create virtual environment:

```bash
python -m venv venv
```

Activate environment:

### Windows

```bash
venv\Scripts\activate
```

### Linux / Mac

```bash
source venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Launch Jupyter Notebook:

```bash
python -m notebook
```

---

# Requirements

Main libraries used:

* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-learn
* SciPy
* Jupyter

---

# Example Workflow

```python
import pandas as pd

df = pd.read_csv("data/ticks_wed.csv")

rolling_vol = (
    df["price"]
    .pct_change()
    .rolling(window=100)
    .std()
)
```

---

# Collaboration Workflow

This repository follows a branch-based collaboration workflow.

## Important Rules

* `main` branch is the stable production branch.
* Do NOT push unfinished or experimental code directly to `main`.
* Each team member must create and work on their own branch.

Example:

```bash
git checkout -b your-name-work
```

---

## Workflow

1. Pull latest changes from `main`
2. Work on your personal branch
3. Commit changes regularly
4. Push your branch to GitHub
5. Open a Pull Request before merging into `main`

---

## Example Commands

### Create your branch

```bash
git checkout -b your-name-work
```

### Push your branch

```bash
git push -u origin your-name-work
```

### Pull latest main updates

```bash
git checkout main
git pull origin main
```

---

## Important

Do not overwrite or directly edit another member's branch without coordination.

The `main` branch should always remain clean, runnable, and presentation-ready.

---

# Quantitative Insights

Key observations from the project include:

* Reconstruction-error spikes often precede unstable market states
* Streaming PCA captures evolving latent market structure
* Volatility clustering reveals regime persistence
* Anomaly thresholds require careful calibration to avoid excessive false positives
* Rolling covariance shifts correlate strongly with labeled anomaly windows

---

# Technologies Used

| Category             | Tools               |
| -------------------- | ------------------- |
| Programming          | Python              |
| Data Analysis        | NumPy, Pandas       |
| Visualization        | Matplotlib, Seaborn |
| Machine Learning     | Scikit-learn        |
| Scientific Computing | SciPy               |
| Development          | Jupyter Notebook    |

---

# Team Members

* Tiya
* Tejasvini
* Yogita

---

# Future Improvements
