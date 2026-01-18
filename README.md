# amazon-smartphone-review-analysis
NLP-based analysis of Amazon smartphone reviews using S-O-R framework
# Amazon Smartphone Customer Review Analysis (NLP + S-O-R)

This repository contains the code and selected outputs for an MSc Business Analytics dissertation titled:

**Customer Review Analysis of Amazon Smartphone Products Using Named Entity Recognition (NER), Topic Modelling, and Sentiment Analysis: A Stimulus–Organism–Response (S-O-R) Perspective.**

## Business Case (Why this matters)
Online reviews are a major driver of customer trust and conversion in e-commerce. For smartphone products—where performance, compatibility, and condition are difficult to verify before purchase—review text provides high-value signals about product failures, service issues, and customer expectations.

This project converts large-scale unstructured review text into **actionable insights** to support:
- **Manufacturers & product teams:** identify recurring quality and reliability pain points  
- **Customer experience & operations teams:** detect service failures (returns/refunds/logistics)  
- **E-commerce marketplace managers:** strengthen customer trust and seller governance  

## Analytical Framework (S-O-R)
The pipeline is structured using the **Stimulus–Organism–Response** lens:
- **Stimulus:** what customers talk about (themes from topic modelling + entities from NER)  
- **Organism:** how customers feel (sentiment polarity and intensity)  
- **Response:** what customers do (star ratings as behavioural evaluation)  

## Methods Used
- **Sentiment Analysis:** VADER (`sentiment_score`, `sentiment_label`)
- **Topic Modelling:** BERTopic (reduced to **12 consolidated smartphone themes**)
- **Named Entity Recognition:** spaCy NER applied to negative reviews with filtered entity types (ORG / PRODUCT / GPE)

## Dataset
**Amazon Reviews: Unlocked Mobile Phones (Kaggle)**  
License: **CC0 (Public Domain)**  
Dataset link: https://www.kaggle.com/datasets/PromptCloudHQ/amazon-reviews-unlocked-mobile-phones

> **Note:** The full dataset (`Amazon_Unlocked_Mobile.csv`) is not included in this repository due to size.  
> A small sample is included in `data/sample_reviews.csv` for demonstration.

## Repository Structure
- `Amazon_Smartphone_Review_Analysis.ipynb` → main Jupyter Notebook  
- `outputs/` → processed outputs used in the report (topic summaries, NER entity table, etc.)  
- `figures/` → exported plots for GitHub and dissertation use  
- `data/` → sample dataset + instructions  
- `requirements.txt` → dependencies for reproducibility  

## How to Run (Reproduce Results)

### 1. Install dependencies
```bash
pip install -r requirements.txt
python -m spacy download en_core_web_sm
```
### 2. Download dataset

Download the Kaggle dataset and place it in the project root as:
Amazon_Unlocked_Mobile.csv

### 3. Run the analysis

Open and run:
Amazon_Smartphone_Review_Analysis.ipynb

## Key Outputs (What to look at)

Theme frequency (most discussed smartphone aspects)

Theme-level pain points (% negative sentiment)

Average rating by smartphone theme

Filtered NER entities appearing in negative reviews

## Academic Use

This repository is provided to support transparency and reproducibility of dissertation findings.  
All analysis is performed at an aggregate level using publicly available review data.

## Author

Rose Bijo — MSc Business Analytics



