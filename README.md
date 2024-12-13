# Developing a Robust NLP Pipeline for German-Language Medical Dialogues in Emergency Settings

This repository contains the code and resources used for the research paper:  
**"Developing a Robust NLP Pipeline for German-Language Medical Dialogues in Emergency Settings"**

## Abstract

**Background**  
Accurate and rapid documentation of patient information is crucial in emergency healthcare settings. Traditional manual methods are time-consuming and error-prone, risking compromised patient outcomes. Recent advances in Large Language Models (LLMs) offer promising solutions, but their application in clinical environments, especially for non-English languages like German, poses challenges related to accuracy, clinical relevance, and privacy. Research addressing these challenges, particularly in German-language emergency contexts, remains limited.

**Objective**  
This study focuses on deploying Natural Language Processing (NLP) tools for German-language emergency medical documentation. The key objectives are:  
1. Developing a robust methodology for generating synthetic, medically accurate dialogues with known ground truth data to validate NLP systems.  
2. Designing a precise pipeline capable of extracting essential clinical information from these dialogues for emergency protocols.  

**Methods**  
- **Data**: Selected 100 anonymized patient records from the MIMIC-IV-ED dataset, using the Post Randomization Method (PRAM) to maintain utility while ensuring privacy.  
- **Synthetic Dialogue Generation**: Utilized the "Zephyr-7b-beta" model for generating coherent dialogues in multiple languages, translated into German using GPT-4 Turbo.  
- **Feature Extraction**: Built a Retrieval-Augmented Generation (RAG) system to extract key features like diagnoses and vital signs.  
- **Evaluation Metrics**: Precision, recall, and F1-scores were used for quantitative assessment, alongside manual evaluation for sentiment and clinical relevance.

**Results**  
- Generated 100 synthetic dialogues, averaging 2,000 tokens in English and 4,000 tokens in German.  
- Observed a sentiment shift in German dialogues (positive sentiment increased from 27% to 38%), which impacted text extraction accuracy.  
- The RAG-based system initially achieved F1-scores ranging from 86.21% to 100%. However, longer dialogues and sentiment changes introduced noise, reducing precision for key features like "Diagnosis" (60.82%) and "Pain Score" (57.61%).

**Conclusions**  
The pipeline demonstrates strong performance in handling structured data and improving documentation efficiency in multilingual environments. However, challenges remain in addressing nuanced clinical language and sentiment shifts in German texts. Future work will focus on refining the system to handle longer dialogues, reduce noise, and improve extraction accuracy.

**Keywords**: Emergency medicine; Large Language Models (LLMs); Dialogue generation; Retrieval-Augmented Generation (RAG); Medical text extraction; Healthcare documentation; NLP in healthcare; Synthetic medical data.

---

## Repository Contents

- **`data/`**: Contains sample synthetic dialogues and anonymized patient records (if applicable).  
- **`models/`**: Pre-trained and fine-tuned models used for dialogue generation and feature extraction.  
- **`scripts/`**: Python scripts for generating synthetic dialogues, RAG-based feature extraction, and evaluation.  
- **`notebooks/`**: Jupyter Notebooks for exploratory data analysis and model performance evaluation.  
- **`results/`**: Evaluation metrics and analysis of pipeline performance.  

---
