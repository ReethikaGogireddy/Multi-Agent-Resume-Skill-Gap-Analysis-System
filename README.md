# Multi-Agent-Resume-Skill-Gap-Analysis-System

## Overview
This project builds a multi-agent system for resume-job matching, skill gap analysis, and career recommendation generation. Instead of relying only on keyword matching, the system extracts structured skills from resumes and job descriptions, compares them using semantic similarity and rule-based reasoning, and produces actionable recommendations for job seekers.

The project also includes classical machine learning baselines to compare modular agentic reasoning with traditional predictive models.

## Problem Statement
Traditional resume screening systems often depend on keyword matching, which can miss relevant transferable skills and deeper semantic relationships. As a result, qualified candidates may be overlooked, and job seekers receive limited guidance on how to improve their fit for specific roles.

This project addresses that issue by using a modular multi-agent architecture that:
- extracts structured skills from resumes
- identifies job requirements from postings
- performs skill-gap analysis
- recommends improvements for better job alignment

## Objectives
- Build a Resume Skill Extraction Agent
- Build a Job Requirement Extraction Agent
- Build a Skill Gap & Recommendation Agent
- Compare the multi-agent system with baseline classifiers such as kNN and Decision Tree
- Evaluate accuracy, interpretability, and practical usefulness

## System Architecture
The system is organized into the following modules:

1. **Preprocessing Layer**
   - text cleaning
   - normalization
   - tokenization
   - lemmatization
   - stopword removal

2. **Resume Skill Extraction Agent**
   - extracts skills from resume text using phrase matching and a curated skill dictionary
   - standardizes skills into a shared schema

3. **Job Requirement Extraction Agent**
   - extracts required and preferred skills from job descriptions
   - maps job requirements into the same normalized skill space

4. **Shared Representation Layer**
   - TF-IDF features
   - sentence-transformer embeddings
   - normalized skill dictionary

5. **Skill Gap Analysis Agent**
   - compares resume skills and job skills
   - classifies skills as matched, partially matched, or missing
   - computes semantic similarity

6. **Recommendation Agent**
   - prioritizes missing skills
   - generates personalized recommendations for skill improvement

7. **Baseline Models**
   - k-Nearest Neighbors (kNN)
   - Decision Tree classifier

8. **Evaluation Layer**
   - extraction quality metrics
   - classification performance metrics
   - qualitative and robustness analysis

## Datasets
### 1. LinkedIn Jobs Dataset
Used for job descriptions, role requirements, and skill demand patterns.
https://www.kaggle.com/datasets/joykimaiyo18/linkedin-data-jobs-dataset?utm_source=chatgpt.com

### 2. Resume Dataset
Used for resume text, category labels, and skill extraction experiments.
https://www.kaggle.com/datasets/jillanisofttech/updated-resume-dataset

## Preprocessing
The following preprocessing steps are applied:
- lowercasing
- punctuation and special-character removal
- stopword removal
- lemmatization
- phrase-based skill extraction
- skill normalization
- TF-IDF feature generation
- sentence embedding generation

## Methods
### Resume Skill Extraction
Skills are extracted from resumes using spaCy-based preprocessing, phrase matching, and a curated skill dictionary.

### Job Requirement Extraction
The same preprocessing pipeline is applied to job descriptions to extract normalized skill requirements.

### Skill Gap Analysis
Resume skills and job skills are compared using:
- exact skill overlap
- semantic similarity in embedding space
- ranking of missing skills based on relevance and frequency

### Recommendation Generation
The system produces actionable recommendations such as:
- which missing skills to learn first
- which projects or certifications to pursue
- how to better present existing skills on a resume

### Baseline Classification
Structured skill features are used to train:
- kNN classifier
- Decision Tree classifier

These baselines help assess whether extracted skill features capture meaningful job distinctions.

## Evaluation
The project is evaluated using:

### 1. Skill Extraction Performance
- Precision
- Recall
- F1-score

### 2. Skill Gap Analysis Quality
- skill coverage
- missing skill detection accuracy
- cosine similarity quality
- ranking consistency

### 3. Baseline Model Performance
- accuracy
- precision
- recall
- F1-score
- confusion matrix

### 4. Qualitative Evaluation
- clarity of recommendations
- actionability of suggestions
- robustness to resume formatting and writing style


## Project Structure
```bash
multi-agent-resume-screening/
├── README.md
├── requirements.txt
├── main.py
├── config.yaml
├── data/
├── notebooks/
├── src/
├── skills/
├── outputs/
└── tests/

## Instructions:
All files in gdrive as we are using colab
