# Assignment-Topsis-for-pre-trained-models
# **Text Classification Model Selection using TOPSIS**

**Author:** Kanika Dhamija  
**Institute:** Thapar Institute of Engineering and Technology, Patiala  
**Roll Number:** 102313062  

---

## **Project Overview**

Text classification is a fundamental task in Natural Language Processing (NLP) used in applications such as sentiment analysis, spam detection, topic categorization, and information filtering.

In this project, multiple lightweight pre-trained transformer models were evaluated for text classification using the AG News dataset from Hugging Face. The best-performing model was selected using the **TOPSIS (Technique for Order Preference by Similarity to Ideal Solution)** multi-criteria decision-making method.

---

## **Objective**

- Evaluate multiple pre-trained transformer models for text classification  
- Compare models using multiple evaluation metrics  
- Apply the TOPSIS method to rank models objectively  
- Identify the most suitable model for deployment in a Colab environment  

---

## **Dataset**

**Dataset Used:** AG News  
**Source:** Hugging Face Datasets Library  
**Samples Used:** 300 test samples  

Each data point contains:
- `text`
- `label` (4 classes)

No fine-tuning was performed. Models were evaluated directly using Hugging Face pipelines.

---

## **Pre-trained Models Evaluated**

- `distilbert-base-uncased`
- `google/electra-small-discriminator`
- `albert-base-v2`
- `bert-base-uncased`

These models were selected due to their lightweight architecture and suitability for quick inference in Colab environments.

---

## **Evaluation Criteria (TOPSIS Parameters)**

| Criterion | Type |
|------------|--------|
| Accuracy | Benefit (+) |
| Macro F1 Score | Benefit (+) |
| Inference Time Per Sample (s) | Cost (−) |
| Model Size (MB) | Cost (−) |
| Computational Cost | Cost (−) |

---

## **Evaluation Methodology**

1. Loaded AG News dataset from Hugging Face.
2. Selected 300 test samples.
3. Used Hugging Face `pipeline()` for text classification.
4. Explicitly converted dataset columns to Python lists for compatibility.
5. Measured:
   - Accuracy
   - Macro F1 Score
   - Inference Time Per Sample
   - Model Size
   - Computational Cost
6. Stored all results in CSV files.
7. Applied TOPSIS to determine final ranking.

---

## **Model Performance Summary**

| Model | Accuracy | Macro F1 | Inference Time (s) | Model Size (MB) |
|--------|----------|-----------|--------------------|------------------|
| distilbert-base-uncased | 0.85+ | 0.84+ | Low | ~260 MB |
| google/electra-small-discriminator | 0.88+ | 0.88+ | Very Low | ~42 MB |
| albert-base-v2 | 0.73+ | 0.72+ | Low | ~45 MB |
| bert-base-uncased | 0.86+ | 0.85+ | Higher | ~438 MB |

---

## **TOPSIS Ranking Results**

| Rank | Model | TOPSIS Score |
|------|--------|--------------|
| 1 | google/electra-small-discriminator | 0.9167 |
| 2 | albert-base-v2 | 0.5385 |
| 3 | distilbert-base-uncased | 0.4871 |
| 4 | bert-base-uncased | 0.0641 |

---



---



---

## **Best Performing Model**

**Best Model:** `google/electra-small-discriminator`

### Why?
- Highest Accuracy
- Highest Macro F1 Score
- Lowest Inference Time
- Smallest Model Size
- Highest TOPSIS Score

It provides the best balance between performance and computational efficiency.

---

## **Conclusion**

This project demonstrates how multi-criteria decision-making techniques like TOPSIS can be effectively applied to select the best machine learning model.

Among the evaluated models, `google/electra-small-discriminator` emerged as the most efficient and accurate model for text classification in a resource-constrained Colab environment.

---

## **Technologies Used**

- Python  
- Hugging Face Transformers  
- Hugging Face Datasets  
- Scikit-learn  
- NumPy  
- Pandas  
- Matplotlib  
- Seaborn  

---
