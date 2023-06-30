 ---
# Classification Models for Indian District Courts Data

This repository contains the implementation of two classification models applied to a database of approximately 80 million Indian district court records. The dataset was obtained from the [Development Data Lab](https://www.devdatalab.org/) and encompasses various features related to case details.

## *Problem Statement*
---
The objective of this project was to explore and develop classification models for predicting and analyzing various aspects of Indian district court cases. The specific classification problem chosen was to predict case resolution time and case disposition based on the available features.

## *Dataset Overview*
---
The dataset comprises records from Indian district courts across multiple states. 

The key features used for classification include state code, district code, court number, judge position, gender of defendant's advocate, gender of petitioner's advocate, case type, case purpose, disposition name, act, section, and number of sections in the Indian Penal Code (IPC) (for cases in India). Additional features such as case completion time, judge's gender, and judge's experience were also considered in the analysis.

## *Classification Models*
---
Two classification models were implemented to address the classification problem:

1. **_Case Resolution Time Classification_**: A separate random forest classification model was developed to categorize the duration of case resolution into five distinct time categories: `1-100 days`, `100-500 days`, `500-1000 days`, `1000-1500 days`, and `1500+ days`. The model achieved an accuracy score of 79% after parameter optimization, providing valuable insights into case resolution time prediction.

    >Contents
    - case_duration.ipynb: Jupyter Notebook for the classifier
    - data_preprocessing_1.ipynb: Jupyter Notebook for pre-processing the data(step 1)
    - data_preprocessing_2.ipynb: Jupyter Notebook for pre-processing the data(step 2)
    - confusion_matrix.png: Confusion Matrix for the model results on the Test Set
    

2. **_Case Disposition Classification_**: A random forest classification model was trained to predict the disposition of a case, classifying it as either a `conviction` or an `acquittal` based on the available features. The model achieved an accuracy score of 88%, demonstrating its effectiveness in predicting case dispositions.

    >Contents
    - case_disposition.ipynb: Jupyter Notebook for the classifier
    - data_preprocessing.ipynb: Jupyter Notebook for pre-processing the data
    - confusion_matrix.png: Confusion Matrix for the model results on the Test Set


## *Insights*
---
1. **_Case Resolution Time Patterns_**: The case resolution time classification model revealed interesting patterns and trends in case resolution durations. It identified that the state code, court number, judge position, gender of defendant's advocate, case type, and specific sections of the act played significant roles in determining the time taken to resolve a case. These insights can assist in managing case backlogs, improving judicial efficiency, and facilitating better resource allocation within the Indian district court system.

2.  **_Case Disposition Analysis_**: By applying the case disposition classification model, it was discovered that the gender of defendant, gender of defendant's advocate, gender of petitioner's advocate, case type,  judge's gender, and experience of the judge significantly influenced the disposition outcome. The insights gained from this model can help legal professionals and stakeholders assess the likelihood of conviction or acquittal based on various case characteristics.


## *Usage and Replication*
---
To replicate the classification models or further explore the dataset, follow the steps below:

1. Obtain the dataset from the Development Data Lab or use a comparable Indian district court dataset.
2. Preprocess the data by selecting the relevant features (as described in the dataset overview).
3. Implement the random forest classification models using suitable machine learning frameworks or libraries.
4. Train the models on the preprocessed dataset and optimize the parameters for improved accuracy.
5. Evaluate the models using appropriate evaluation metrics and analyze the results.
6. Further refine and expand the models by incorporating additional features or applying different classification algorithms if desired.

>Please note that the models described here are based on a specific dataset and problem statement. Adaptations may be necessary depending on the specific dataset and classification problem being addressed.

## *Dependencies*
---
```
Pandas
NumPy
Seaborn
Sklearn
```
