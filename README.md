# sentiment-analyzer-with-DAN-and-LTSM

# Sentiment Analyzer Using Deep Learning (Word2Vec + BiLSTM)

This project is a deep learning–based sentiment classification system trained on real-world book reviews. The goal was to explore the effectiveness of pretrained embeddings and sequence-aware models (DAN vs. Bidirectional LSTM) for understanding user sentiment in long-form natural language.

> Completed as part of the Breakthrough Tech AI Program — optimized for showcase in industry-grade ML portfolios.

---

## Project Highlights

- **Domain**: NLP, Sentiment Analysis  
- **Dataset**: 10,000+ book reviews (binary sentiment)  
- **Tech**: Keras, Word2Vec, LSTM, Sequential API  
- **Evaluation**: Accuracy, F1 Score, Confusion Matrix, ROC-AUC  
- **Best Model Performance**: 75% test accuracy with AUC = 0.61

---

## Motivation

Traditional classifiers often struggle with nuanced, long-form reviews. My aim was to:
- Explore how **word embeddings** (Word2Vec) capture semantic meaning
- Compare lightweight vs. sequence-aware models (DAN vs. BiLSTM)
- Tune deep models for generalization while avoiding overfitting

---

## Models Implemented

### Deep Averaging Network (DAN)
- Averages pretrained Word2Vec vectors
- Simple and fast but lacks word order sensitivity

### Bidirectional LSTM (Tuned)
- Captures both past and future context
- Fine-tuned using dropout, early stopping, and embedding adaptation

---

## ⚙Techniques Used

- **Text Preprocessing**: Stopword removal, custom cleaning (no external NLP tools)
- **Embeddings**: Trained custom Word2Vec model on domain corpus
- **Model Tuning**: Dropout, patience, hidden units, trainable embeddings
- **Train/Val/Test Split**: 60/20/20 with stratification
- **Evaluation**: 
  - Accuracy and loss curves
  - Confusion matrix and F1 scores
  - ROC-AUC curve analysis

---

## Results

| Model     | Val Accuracy | Test Accuracy | AUC   | F1 Score |
|-----------|--------------|----------------|-------|----------|
| DAN       | ~57%         | ~58%           | 0.55  | 0.52     |
| BiLSTM    | ~75%         | **75%**        | 0.61  | 0.54     |

---
## Future Improvements

- Experiment with GRUs or attention mechanisms
- Incorporate explainability (e.g., SHAP for text)
- Explore transformer-based models like BERT

---

## About Me

I'm a Breakthrough Tech AI Fellow passionate about applying machine learning to solve real-world NLP problems.  
This project was built to demonstrate my end-to-end ML skills — from data prep to evaluation — and is portfolio-ready for roles in machine learning and AI engineering.


