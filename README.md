# Music Recommender System with Audio Features and NLP

This project combines numerical audio features and Natural Language Processing (NLP) to build a personalized music recommender system. The goal is to enhance recommendations by analyzing both the musical and lyrical content of songs.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Dataset Sources](#dataset-sources)
- [Technologies](#technologies)
- [How It Works](#how-it-works)
- [Results](#results)
- [Usage](#usage)
- [Author](#author)

## Introduction

With the rise of music streaming platforms, recommendation systems have become essential to improve user experience. Most systems focus solely on acoustic properties or user behavior. This project proposes a hybrid system that incorporates:

- Numerical audio features (e.g., energy, danceability, tempo)
- Lyrics analysis using NLP (e.g., thematic content of songs)

This approach aims to provide more accurate and emotionally aligned recommendations.

## Features

- Extract audio features like energy, valence, and tempo.
- Analyze song lyrics using a pre-trained DistilBERT model.
- Predict musical subgenres using a Random Forest Classifier.
- Combine genre and lyric topic predictions to recommend songs.
- Exploratory Data Analysis on musical habits and mental health.

## Dataset Sources

- https://www.kaggle.com/datasets/joebeachcapital/30000-spotify-songs
- https://www.kaggle.com/datasets/saurabhshahane/music-dataset-1950-to-2019
- https://www.kaggle.com/datasets/catherinerasgaitis/mxmh-survey-results

## Technologies

- Python
- Pandas, NumPy, Scikit-learn
- Hugging Face Transformers (DistilBERT)
- Joblib
- Matplotlib, Seaborn
- Google Colab

## How It Works

1. Preprocess audio features: clean and scale the dataset.
2. Predict subgenre: use a trained Random Forest Classifier.
3. Analyze lyrics: predict topic using DistilBERT tokenizer and model.
4. Filter recommendations: return top songs that match both the predicted subgenre and lyrical theme.

If no match is found for the lyrics topic, the system falls back to genre-only filtering.

## Results

- The Random Forest model showed high accuracy for genre prediction.
- The DistilBERT-based NLP model extracted lyrical themes effectively, adding another layer to personalization.
- Combining both models produced more nuanced recommendations.

## Usage

This project was developed in Jupyter notebooks. You can test the system by cloning the repo and running the following notebooks:

- `recomendador.ipynb`: Core recommender pipeline
- `modeloLyrics.ipynb`: Lyrics topic classification with DistilBERT

Requirements: Python 3.9+, Transformers, Scikit-learn

## Author

David Alfonso Barbosa Gómez  
davidbarbosagomez@hotmail.com  
[LinkedIn](https://www.linkedin.com/in/david-alfonso-barbosa-g%C3%B3mez-a41215339/)  
[GitHub](https://github.com/DavidBarbosag)

This project was developed as part of my academic work at Escuela Colombiana de Ingeniería Julio Garavito (2024).
