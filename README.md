# Capstone-3-Documentation

## Project Overview
This project predicts whether a piece of writing was created by an AI or a human using **only numeric readability/style metrics** and **categorical content type**.  
No raw text analysis is used — instead, the model relies on structured features to detect differences.

---

## Dataset
**File:** `ai_human_content_detection_dataset.csv`  
- **Numeric features:** word_count, character_count, sentence_count, lexical_diversity, avg_sentence_length, avg_word_length, punctuation_ratio, flesch_reading_ease, gunning_fog_index, grammar_errors, passive_voice_ratio, predictability_score, burstiness, sentiment_score  
- **Categorical feature:** content_type  
- **Target:** `label` (0 = Human, 1 = AI)

**Source:** Custom Kaggle dataset (2025)

---

## Methodology
1. Dropped raw text content  
2. Scaled numeric features  
3. One-hot encoded `content_type`  
4. Combined numeric + categorical features  
5. Train/Test split (80/20)  
6. Trained Logistic Regression, Random Forest, and XGBoost models  
7. Evaluated with Accuracy, Precision, Recall, F1-score  

---

## Results

| Model               | Accuracy | Precision | Recall | F1-score |
|---------------------|----------|-----------|--------|----------|
| Logistic Regression | 0.85 | 0.84 | 0.83 | 0.835 |
| Random Forest | 0.9 | 0.91 | 0.89 | 0.9 |
| XGBoost | 0.93 | 0.94 | 0.92 | 0.93 |


---

## EDA Visuals
**Class Distribution**
![Class Distribution](class_distribution.png)  

**Correlation Heatmap**
![Correlation Heatmap](correlation_heatmap.png)  

---

## Key Findings
- **XGBoost** achieved the highest accuracy (~0.93)  
- **Random Forest** performed well (~0.90)  
- **Logistic Regression** slightly less accurate (~0.85)  
- Numeric and categorical features alone can detect AI-generated text effectively  

---

##  Conclusion
Structured writing metrics can distinguish AI-generated text from human-written text without using raw content.  
Applications include:
- Plagiarism detection
- Content moderation
- Authorship verification
- Journalism integrity

---

##  Project Files
- `Capstone3_Final_Report.docx` – Detailed report  
- `Capstone3_Presentation.pptx` – 8-slide presentation  
- `model_metrics.csv` – Model performance metrics  
- `class_distribution.png` – Class distribution plot  
- `correlation_heatmap.png` – Feature correlation heatmap  

---
