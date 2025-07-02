# Real-Time Fake News Detection in Mainstream Media

---

## 📌 Project Objective

The primary goal of this project is to build a real-time fake news detection system that can classify news from mainstream sources, such as TV and radio as real or fake. The system accepts user inputs in the form of recorded audio or captured images, processes the extracted text using Natural Language Processing (NLP) techniques, and performs classification using a fine-tuned BERT model.

---

## Methodology

The system provides two pathways for input:
1. **Speech-to-Text**: Audio from news broadcasts is recorded, transcribed using speech recognition APIs, and converted to text.
2. **Image OCR**: News headlines from TV screens or online media are captured and processed using OCR to extract textual information.

The cleaned and preprocessed text is then classified using a BERT-based model, which has been trained on a curated and balanced dataset.

---

## Models Used

- **RNN (Recurrent Neural Network)**: Used during initial experimentation and training phases for sequence modeling of text data.
- **BERT (Bidirectional Encoder Representations from Transformers)**: A transformer-based NLP model fine-tuned for binary classification of news as real or fake. It is a state-of-the-art contextual model thatleverages bidirectional context understanding for improved accuracy.

---

## 📊 Data Used

- A dataset comprising approximately 25,000 news articles.
- **Real news** was sourced from verified publishers like Reuters
- **Fake news** was sourced from fact-checking websites such as PolitiFact
- Most of the dataset revolves around topics like US elections and world politics.

Preprocessing included stopword removal, lowercasing, punctuation removal, and merging of title and body text.

---

## 📁 File Description

- `Fake News RNN_Detection.ipynb`  
  Script for training an RNN model on the labeled fake/real news dataset. It includes preprocessing steps and training loops.

- `Fake_News_Extraction_BERT_Paramters.ipynb`  
  Includes:
  - Captures input via microphone or image upload.
  - Transcribes audio using speech recognition or extracts text using OCR (Tesseract).
  - Applies the trained BERT model to classify the news as real or fake.

---

## Results

- **Accuracy:** 96.55% on the test set.
- **F1 Score:** 0.9655
- **ROC AUC:** 0.965
- The model showed robust performance with both custom and test inputs, particularly when complete text (headline + body) was provided.

---


## References

- [BERT Model Paper](https://arxiv.org/abs/1810.04805)
- [Tesseract OCR](https://nanonets.com/blog/ocr-with-tesseract/)
- Speech Recognition API: Google Speech-to-Text


