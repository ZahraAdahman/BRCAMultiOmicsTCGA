# Genomic Data Science
## BRCAMultiOmicsTCGA

## Project title: 
'FOXA1 Data analysis of TCGA-BRCA dataset on Breast Invasive Carcinoma' - By Zahra Adahman.

![BRCA_IntroImage](https://github.com/user-attachments/assets/60f2d293-94da-4d63-9168-7e82a50a8102)

#### Nov/Dec 2024.
The python code is in the **master branch**

## Background and Problem

Forkhead box A1 (FOXA1) is a transcription factor that plays a key role in the development and progression of breast cancer. FOXA1 is a pioneer factor that binds to chromatin, allowing other transcription factors to bind to DNA. FOXA1 is especially important in lobular breast cancer, where it's overrepresented and associated with tumor progression.
This project aims to understand the relationship between the mutations in FOXA1 relative to vital status, other genetic mutations and well as other features in breast cancer cases from an NIH-NCI database, TCGA-BRCA.

## Methodology 

* Python
* Jupyter Notebook
* Pandas Library
* Numpy Library 
* Seaborn Library
* ScikitLearn Library-Kmeans, PCA


## Data
The dataset was downloaded from Kaggle: https://www.kaggle.com/datasets/0425b3af5246404d92316a6887a58e40421619498d8f6fe04633181bd6560830
The original dataset processed by https://rbabaei82.github.io/MultiOmics_TCGA-BRCA/Analysis from NCI-TCGA-BRCA database: https://portal.gdc.cancer.gov/projects/TCGA-BRCA

## Data Visualization 
### Kmeans clustering on PCA transformed scaled data.
![image](https://github.com/user-attachments/assets/2007a5f8-644d-4cde-9a4e-e0e9a37e9971)


#### Vital Status 
![image](https://github.com/user-attachments/assets/101c7764-372c-480e-8e8d-99705f3768c0)
#### Mutations in FOXA1
![image](https://github.com/user-attachments/assets/b66003cf-ca85-4c0e-8b1d-a3e587b787b0)
#### Estrogen Receptor Status_Positive
![image](https://github.com/user-attachments/assets/8c3a63ec-2711-40a0-92d1-6d9ebe76846c)

Cluster 2 has the lowest vital status, ER.status_Positive, and a lower mutation in FOXA1, compared to cluster 0 which has the highest ER.status_Positive.
While cluster 1 has the highest vital status, no ER.status (negative or undetermined) and lower FOXA1 mutation compared to cluster 2.
Studies have shown that FOXA1 governs the estrogen-regulated transcriptome and cell growth in breast cancer. 
Cluster 2 has lower ER.status_Positive, and a lower mutation in FOXA1, as FOXA1 is required for estrogen expression. 
Hurtado A.et al FOXA1 is a key determinant of estrogen receptor function and endocrine response. 2011.
Robinson et al. FoxA1 is a Key Mediator of Hormonal Response in Breast and Prostate Cancer. 2012.

#### The best performing model is Random Forest with an accuracy of 0.9018.
![image](https://github.com/user-attachments/assets/924bd596-d303-43c8-87fa-6e3f744db57d)

## Conclusion
1. Considering the dataset was smaller after cleaning and removing cases with missing features from the TCGA-BRCA data
2. Another K means clustering analysis without using PCA prior. 
3. The next step will be acquire more data for modeling a predictor for vital status based on the FOXA1 mutation in breast carcinoma cases.
