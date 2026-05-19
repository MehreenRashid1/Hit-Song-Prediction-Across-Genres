# Hit Song Prediction Across Genres: A Domain-Shift and Feature Importance Analysis Using Spotify Audio Features

This project examines how well machine learning models trained on one musical genre can predict hit songs in other genres — a problem framed as **domain shift**. Using the Spotify Tracks Dataset, genres are treated as separate domains and a suite of experiments is run to measure cross-genre generalization gaps and identify which audio features drive popularity universally versus in genre-specific ways.

---

## Experiments

| # | Experiment | Description |
|---|---|---|
| 1 | Within-Genre LR (Baseline) | L2 Logistic Regression trained and tested within each genre |
| 2 | Cross-Genre Domain Shift | Models tested across genres to measure generalization gap |
| 3 | L1 Feature Selection | L1 regularization to identify universal vs. genre-specific features |
| 4 | Random Forest Feature Importance | RF importance scores compared against L1 findings |
| 5 | PCA + Logistic Regression | Dimensionality reduction before classification |
| 6 | PLS + Logistic Regression | Target-aware compression before classification |

---

## Requirements

```bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
```

---

## Dataset

Download the **Spotify Tracks Dataset** from Kaggle and place it in the project root as `dataset.csv`.

> https://www.kaggle.com/datasets/maharshipandya/-spotify-tracks-dataset

---

## How to Run

### Option 1 — Jupyter Notebook
```bash
# Clone the repo
git clone https://github.com/your-username/spotify-hit-analysis.git
cd spotify-hit-analysis

# Install dependencies
pip install -r requirements.txt

# Launch the notebook
jupyter notebook spotify_hit_analysis.ipynb
```

### Option 2 — VS Code
1. Clone the repo and open the folder in VS Code
2. Install the **Jupyter** extension from the VS Code marketplace
3. Open `spotify_hit_analysis.ipynb`
4. Select your Python interpreter and run all cells

### Option 3 — Google Colab
1. Go to [colab.research.google.com](https://colab.research.google.com)
2. Click **File → Upload Notebook** and upload `spotify_hit_analysis.ipynb`
3. Upload `dataset.csv` to the Colab session storage or mount your Google Drive
4. Run all cells from top to bottom

Run all cells from top to bottom. Each section builds on the previous one so order matters.