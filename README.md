# Content-Based Medical Image Retrieval (CBMIR) System

## Overview
This repository contains the implementation of a Content-Based Medical Image Retrieval (CBMIR) system. The system integrates cutting-edge technologies to deliver highly relevant search results based on image and text data.

## Methodology
The CBMIR system is implemented using the following methodology:

### 1. Dataset and Preprocessing
- The dataset used is the chest x-rays dataset from Indiana University, consisting of 6 columns: image name, image caption, comparison, indication, findings, and impression.
- Preprocessing involves replacing synonyms with root words, decontracting words, and removing special characters, numbers, and meaningless words.
- The 'findings' column with the least null values is chosen as the text feature for analysis.

### 2. Auto Encoder
- A Convolutional Auto Encoder (CAE) with a skip layer and a residual block is used for dimensionality reduction and feature extraction from images.
- The CAE architecture includes convolutional layers, max-pooling layers, and dense layers for encoding and decoding.

### 3. TF-IDF and Cosine Similarity
- Term Frequency - Inverse Document Frequency (TF-IDF) is used to convert text into feature vectors.
- Cosine similarity is employed to measure the similarity between image and text feature vectors, enabling efficient retrieval of relevant images.

### 4. Query Processing
- The system accepts user queries in the form of either images or text.
- For image queries, the encoder extracts features and compares them with a grid of image vectors using cosine similarity.
- For text queries, TF-IDF is applied to the query text, and cosine similarity is used to compare with text feature vectors.

### 5. Results
- The system generates ranked lists of relevant images based on query similarity.
- Visualizations such as PDF and CDF plots, word clouds, and loss function graphs are provided to analyze the results and model performance.

### 6. Comparison
- The methodology is compared with other approaches, highlighting advantages in simplicity, versatility, and clarity.

## Conclusion
The CBMIR system provides an efficient and accurate method for retrieving relevant medical images based on content analysis. The methodology outlined here ensures robustness, scalability, and improved user experience.