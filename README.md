# Most streamed Spotify songs Analysis

## Table of Contents
- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools](#tools)
- [Data Cleaning & Preparation](#data-cleaning-and-preparation)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Results and findings](#results-and-findings)
- [Recommendations](#recommendations)
- [Limitations](#limitations)
- [References](#references)
 

### Project Overview
In this project I have performed a complete Data Exploration of the most streamed Spotify songs up to 2024. By analyzing several metrics of Spotify tracks, I aim at identifying trends, records and gain a deeper understanding of the music market's logic.

### Data Sources
The dataset used in this project "Spotify_Refined_Explicity_classifed.csv" was retrieved on [Kaggle](https://www.kaggle.com/datasets/pragyantiwari/spotify-refined-explicity-classified-1). It contains 4600 different tracks and a total of 30 columns that provide with important information per each track, e.g. the release date, the artist, the track score, number of streams etc.

### Tools
The whole data preprocessing and visualization has been performed by means of [Python](https://www.python.org/downloads/) programming language and [Jupyter Notebook](https://jupyter.org/install) platform. It is accessible throughout the "Most Streamed Spotify Songs 2024.ipynb" file.

### Data Cleaning and Preparation
The first step of this project regards the data loading and preprocessing. I performed the following taks:
1. **Data loading and inspection**;
2. **Handling missing values**;
3. **Data cleaning** (drop useless columns and duplicated) and **formatting**.

### Exploratory Data Analysis
Exploratory Data Analysis (EDA) process consists of exploring the dataset to answer key questions, such as:
- How has the number of released tracks changed over the years?
- Does a preferred release month exist?
- What are the most streamed songs and artists on Spotify? What about YouTube and TikTok?
- Do explicit songs have higher "track score" with respect to friendly ones?
- What are the main factors that affect the *track score* ?

## Results and findings
![num_tracks_year](https://github.com/user-attachments/assets/c0a73bac-ff4a-4433-b2aa-a993b99637d5)

![months](https://github.com/user-attachments/assets/b325e110-08f2-47c6-98b9-e5ae585100b9)

![most_streamed_tracks](https://github.com/user-attachments/assets/d767cfe0-08c2-49f9-ac65-283d48d545f1)

![most_streamed_artists](https://github.com/user-attachments/assets/77471030-9b4f-4321-a422-124afa9566b6)


![class_pie](https://github.com/user-attachments/assets/11168980-6044-44e3-a591-172c237c1eed)
![track_score_class](https://github.com/user-attachments/assets/e08232da-1733-46b6-9215-67bdbed2a90d)
![expl_friend_years](https://github.com/user-attachments/assets/51ff3985-04ee-4b19-95ff-4cff39c4a10f)

![df_corr](https://github.com/user-attachments/assets/f59aab19-1845-4a46-8ec4-b1e020a8832a)

## Recommendations

## Limitations

## References
