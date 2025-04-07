#  Early Alzheimer’s Diagnosis Using a Multiview Approach on Genetic and Clinical Data

This project aims to improve the early diagnosis of Alzheimer’s Disease (AD) by combining genetic and clinical data using a multiview deep learning pipeline. 
The method leverages separate autoencoders for feature extraction and applies ensemble classifiers to achieve robust predictions across datasets collected using different technologies.

##  Project Overview

Early diagnosis of Alzheimer's Disease is a major challenge in clinical settings, due to the limited sensitivity of traditional methods. This work explores a **multimodal approach** that integrates:
- **miRNA expression data** (genetic features)
- **Clinical metadata** (age, sex, APOE4)

Each data type is encoded using a dedicated autoencoder, and the resulting embeddings are concatenated and used as input for classification using:
- Random Forest
- Multilayer Perceptron (MLP)

##  Experiments

Three experimental settings were evaluated:
1. **Cross-validation** on a microarray-based dataset.
2. **Cross-dataset** generalization: trained on microarray, tested on high-throughput sequencing (HTS) data.
3. **Train/test split** within the HTS dataset.

Batch sizes of **3** and **256** were tested to study performance and efficiency.

## 💾 Datasets

Two datasets were used:
- `df_microarray`: Aggregated from public datasets using the microarray technique.
- `df_hts`: Based on high-throughput sequencing (HTS).

Class labels:  
- AD (Alzheimer's Disease)  
- MCI (Mild Cognitive Impairment)  
- NC (Normal Control)






