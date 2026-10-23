# News Article Clustering & Recommendation System

A content-based recommendation system using K-Means clustering on Vietnamese news articles, with a Flask web demo.

## Project Overview

This project implements K-Means clustering (including a from-scratch version) to group similar news articles and recommend related content. A simple Flask web application was built to demonstrate the recommendation feature interactively.

**Key Features:**
- Implemented K-Means algorithm from scratch (centroid assignment, centroid revision, heterogeneity calculation, and smart initialization / K-Means++)
- Compared standard K-Means vs K-Means++ using heterogeneity
- Used TF-IDF features for text representation
- Built a Flask web interface for querying similar articles
- Included detailed project reports
- Docker support for easy deployment

## Tech Stack

- **Python 3.8** (required by TuriCreate)
- **TuriCreate** (SFrame & data handling)
- **Scikit-learn** (pairwise distances, normalization)
- **SciPy** (sparse matrices)
- **NumPy & Matplotlib**
- **Flask** (web demo)
- **Docker**

> **Important**: TuriCreate only supports Python 3.5 – 3.8. This project is designed to run on Python 3.8.

## Project Structure
```text
news-clustering-recommendation/
├── app/
│   └── app.py                 # Flask application
├── notebooks/
│   └── kmeans_analysis.ipynb  # Analysis & K-Means experiments
├── data/
│   └── dataset1.csv           # News dataset
├── templates/                 # HTML templates for Flask
├── reports/                   # Project reports (PDF / documents)
├── requirements.txt
├── Dockerfile
└── README.md
```

## How to Run

### Option 1: Run with Docker (Recommended)

```bash
# Build the image
docker build -t news-kmeans .

# Run the container
docker run -p 3333:3333 news-kmeans
```

### Option 2: Run Locally
#### 1. Create and activate environment (Python 3.8 required):  
```bash
conda create -n kmeans-env python=3.8
conda activate kmeans-env
pip install -r requirements.txt
```
#### 2. Run the analysis notebook (optional):
```bash
jupyter notebook notebooks/kmeans_analysis.ipynb
```
#### 3. Run the Flask web demo:
```bash
cd app
python app.py
```
Then open: http://127.0.0.1:3333