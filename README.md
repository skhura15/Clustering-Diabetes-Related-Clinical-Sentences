Clustering Diabetes-Related Clinical Sentences

This repository contains the code, and supporting files for the dissertation "Clustering Diabetes-Related Clinical Sentences in the MIMIC-IV Dataset for Enhanced Semantic Grouping". The project focuses on clustering semantically related clinical sentences from unstructured text, specifically addressing acute issues in diabetic patients.

Project Overview

Electronic Health Records (EHRs) offer transformative potential for healthcare analytics, but their unstructured nature poses significant challenges. This project tackles these issues by:

Preprocessing clinical text data.
Generating domain-specific sentence embeddings using BioSentVec.
Applying clustering techniques to group semantically similar sentences.
Enhancing cluster quality through dimensionality reduction and custom refinement methods.
The analysis is based on the MIMIC-IV Note dataset, a publicly available de-identified database containing extensive clinical notes, including admission notes, discharge summaries, and progress notes.

Key Components

Methodology
Focus: Exclusively analyzed acute issues related to diabetes management.
Preprocessing: Regex-based filtering, tokenization, stopword removal, and handling medical abbreviations.
Sentence Embeddings: Used BioSentVec, a domain-specific model trained on biomedical texts and MIMIC-III data, to generate dense vector representations of clinical sentences.
Dimensionality Reduction: Applied Principal Component Analysis (PCA) to reduce embedding dimensions while preserving 95% variance.
Clustering: Evaluated multiple algorithms, including DBSCAN, HDBSCAN, and Agglomerative Clustering, with DBSCAN providing the best results.
Cluster Refinement: Developed a custom merging function based on cosine similarity to enhance cluster coherence.
Results
DBSCAN emerged as the most effective clustering algorithm, offering high cluster coherence and separation.
Topic modeling (using Latent Dirichlet Allocation) uncovered significant themes within clusters.
Word clouds visualized prominent terms, aiding interpretability.
Applications
Enhanced clinical decision-making by organizing diabetes-related clinical notes for quick access.
Improved understanding of acute diabetes-related issues, supporting personalized treatment plans.
Facilitated the extraction of actionable insights from unstructured clinical text.
Future Work

Expansion to Other Clinical Conditions: Extend the clustering methodology to analyze unstructured clinical notes related to chronic diseases, mental health, or other medical domains.
Real-Time Processing: Develop scalable solutions for real-time clustering and semantic analysis of clinical notes.
Integration with Clinical Decision Support Systems (CDSS): Embed the clustering and analysis techniques into CDSS to assist healthcare providers in generating alerts, trends, and personalized care plans.
Advanced Topic Modeling: Incorporate state-of-the-art models for better extraction of latent topics, improving the granularity of insights.
Semantic Contradiction Detection: Explore techniques to handle contradictory information within clinical notes, a critical factor in ensuring data reliability.
Repository Contents

Code Files:
biosentvec_embeddings.ipynb: Code for generating sentence embeddings using BioSentVec.
clustering_vf.ipynb: Implementation of clustering algorithms and evaluation metrics.
preprocessing_vf.ipynb: Preprocessing steps for cleaning and structuring the MIMIC-IV Note data.
Datasets:
MIMIC-IV Note Dataset (access not included in this repository): A publicly available dataset containing de-identified clinical notes.
Dissertation:



Python 3.8 or later
Libraries: numpy, pandas, scikit-learn, gensim, nltk, h5py, matplotlib, seaborn, and tqdm.

Author
Saanidhya Khurana
