# Water Quality Prediction: Intel OneAPI Hackathon

## Problem statement:
Freshwater is one of our most vital and scarce natural resources, making up just 3% of the earth’s total water volume. It touches nearly every aspect of our daily lives, from drinking, swimming, and bathing to generating food, electricity, and the products we use every day. Access to a safe and sanitary water supply is essential not only to human life, but also to the survival of surrounding ecosystems that are experiencing the effects of droughts, pollution, and rising temperatures. Participants interested in this theme shall use the below mentioned dataset to check the suitability of water for consumption.

The given dataset serves as a valuable resource for this purpose. By leveraging advanced analytics and predictive modeling, we can evaluate the quality of water based on a range of crucial parameters, allowing us to make informed decisions about its fitness for human consumption.
The suggested solution offers comprehensive exploration of various machine learning models and techniques applied to this dataset. From Logistic Regression to Random Forest, Passive Aggressive Classifier, Decision Tree Classifier, AdaBoost, and Neural Network, each model plays a role in evaluating water quality. These analyses offer valuable insights into the performance and effectiveness of different machine learning approaches in solving this critical real-world problem.

## Role of Intel® AI Analytics Toolkit (AI Kit)

During the Intel OneAPI hackathon, the Intel Toolkit empowered us to tackle complex problems more efficiently compared to the regular sklearn library. Its comprehensive set of tools and optimizations allowed us to harness the full potential of modern hardware, achieving significant performance gains and accelerating my project's development.

## Data analysis, visualization and preprocessing:

The provided dataset comprises of **5,956,842** data points, with **23 feature columns** and **1 target** column showing target label (sustainability of sample).

Now, let's take a closer look at the columns:

1.	**Index**: A unique identifier for each row.
2.	**pH:** A numerical value representing the pH level of the water.
3.	**Iron:** A numerical value representing the iron content in the water.
4.	**Nitrate:** A numerical value representing the nitrate content in the water.
5.	**Chloride:** A numerical value representing the chloride content in the water.
6.	**Lead:** A numerical value representing the lead content in the water.
7.	**Zinc:** A numerical value representing the zinc content in the water.
8.	**Color:** Categorical data describing the color of the water, such as "Colorless," "Faint Yellow," etc.
9.	**Turbidity:** A numerical value representing the turbidity of the water.
10.	**Fluoride:** A numerical value representing the fluoride content in the water.
11.	**Copper:** A numerical value representing the copper content in the water.
12.	**Odor:** A numerical value or categorical data describing the odor of the water.
13.	**Sulfate:** A numerical value representing the sulfate content in the water.
14.	**Conductivity:** A numerical value representing the electrical conductivity of the water.
15.	**Chlorine:** A numerical value representing the chlorine content in the water.
16.	**Manganese:** A numerical value representing the manganese content in the water.
17.	**Total Dissolved Solids:** A numerical value representing the total dissolved solids in the water.
18.	**Source:** Categorical data indicating the source of the water, such as "Lake," "River," "Ground," etc.
19.	**Water Temperature:** A numerical value representing the water temperature.
20.	**Air Temperature:** A numerical value representing the air temperature.
21.	**Month:** Categorical data indicating the month when the data was recorded, such as "January," "November," etc.
22.	**Day:** A numerical value representing the day when the data was recorded.
23.	**Time of Day:** A numerical value representing the time of day when the data was recorded.
24.	**Target:** A binary categorical variable (0 or 1) indicating whether the water quality is suitable (1) or unsuitable (0) for consumption.



## PREPROCESSING

### Dealing with null values:
Filling null values with the mode (most frequent value) is a common practice in data preprocessing, and it's often used when dealing with categorical or discrete data. Here are some reasons why filling null values with the mode is a reasonable approach:
•	Preservation of Data Distribution
•	Handling Categorical Data
•	Simplicity and Robustness
•	No Assumption of Linearity
•	Interpretability

### Class Distribution Analysis:
Label imbalance occurs when the number of data points in each class is.
We check of label imbalance which turnrns out to be not roughly equal, leading to a significant difference in class frequencies.

![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/75f37449-8fdd-4689-87e0-1df663676e0a)

### Handling Class Imbalance:
The code addresses class imbalance using the Random Over-sampling technique from the imbalanced-learn library. This technique balances the dataset by oversampling the minority class.
Class distribution after Handling Class Imbalance:
0: 4151590, 
1: 4151590


### The code analyzes the class distribution, which is crucial for binary classification tasks. It visualizes the frequency of each class (suitable and unsuitable water) using a bar plot.
![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/2ca8bd35-9c85-4156-beb0-dab32e7a5d46)
![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/113b61fe-89a9-4957-aa5f-da0f3e0fafc0)
![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/b0302597-b144-44cb-9f02-6472cdb34941)
![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/598eaaa1-977a-4843-8b90-a0a2c2404322)
![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/c44b1dde-1aa1-4ec1-9b08-e8d45163ab1c)
![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/d03c7bae-6b0e-4bdc-98c4-0f88616dccee)
![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/bdb875de-30e6-421f-a0c9-85b2b16ba3a7)
![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/f089946a-d031-4834-9507-7a27704e3298)
![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/bf9b568b-b7fd-48d8-8a5c-9f00f4cd4c37)
![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/95ca3819-8758-4190-a4ba-d0d19091e054)
![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/7814e683-8b7f-4aa1-a5da-b163769f9958)
![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/d1824fa8-a9f5-4344-91ca-cb9af01a38ac)
![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/af468cff-b59d-4f5b-a81c-a0a35798c9f0)
![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/e8a0b0c8-150f-487b-88e4-ae693705fe72)
![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/adedaa12-67ee-410e-9cd1-c053864f9749)
![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/2defb31d-ece9-4e34-8fdd-0db54c09197b)
![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/e473eedd-f0f3-4403-8263-6eecfe7f4400)
![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/0a224bfb-aaf7-4294-831c-4f928e3c6346)
![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/5b0e8570-e443-4036-ac9d-647d48cc9779)
![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/eb38c337-29ee-4a56-95a9-decca8dd8293)


### Data Distribution and Outlier Detection:
The distribution of numerical features is visualized using histograms, showing the density of values for each feature. Additionally, box plots are used to detect outliers in the numerical features.

![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/339e1126-f4bd-4d8a-b10a-5e1a70cbab2c)
![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/7871c985-40ca-47a1-8609-c441316db7d5)
![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/eea2b863-ef78-467a-9b33-923f5c0c5c07)
![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/72457ae1-fdd5-45a6-9aea-c5efe024131c)
![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/7072975d-fc63-4093-84e8-432e68d64f1a)
![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/e39d07a1-38d0-4337-bb16-cdc81a69e627)
![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/6e67f86e-7907-4479-9054-202037b1fcf9)
![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/47e747d6-5bc7-401b-b5f5-a6a986e40d86)
![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/b0026190-971c-430f-8ee0-e1893d0a708e)
![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/f57dab0f-e05c-466e-8fca-3b777b89774e)
![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/5db53919-37a2-441b-b620-0ff042892dde)
![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/7bbb27af-fb48-472e-a131-7f3bf70128f7)
![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/b2604cc8-0d96-4b1a-aa4a-34d43b4d5125)
![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/20b85c77-7315-448e-b2be-1e20f57af318)
![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/09ea5af3-bd6c-443d-aaca-865b3562f9c5)
![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/a8f4059d-ffbb-4670-b725-4f20076dff85)
![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/299c393b-8efb-422c-b091-7fe002c686c3)
![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/044c9131-e86a-43ca-84ce-a47bcecb9f5d)
![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/d7c1d25d-af1a-4cac-b0de-8de5ea529627)


### Encoding Categorical Data:
Categorical columns ('Source,' 'Color,' and 'Month') are encoded into numerical values using Label Encoding, making them suitable for machine learning models.

### Correlation Analysis:
A correlation matrix heatmap is generated to visualize the relationships between numerical features. The heatmap helps identify potential correlations between variables.

![image](https://github.com/dishitamohan/Water_Quality_Prediction_Intel_OneAPI_Hackathon/assets/92173465/c2d32384-eab3-4b86-852c-2f3a160264b1)


### Feature Scaling:
MinMax scaling is applied to standardize the feature values within a specified range.


### Principal Component Analysis (PCA):
PCA is performed to reduce the dimensionality of the dataset while retaining 95% of the variance. This dimensionality reduction can help improve model performance and reduce computational complexity.

## AFTER PREPROCESSING:
the preprocessing steps have transformed the raw dataset into a format suitable for machine learning. This includes handling missing data, encoding categorical features, scaling the data, addressing class imbalance, reducing dimensionality.


## Intel® AI Analytics Toolkit (AI Kit):
The Intel® AI Analytics Toolkit (AI Kit) gives data scientists, AI developers, and researchers familiar Python* tools and frameworks to accelerate end-to-end data science and analytics pipelines on Intel® architectures. The components are built using oneAPI libraries for low-level compute optimizations. This toolkit maximizes performance from preprocessing through machine learning, and provides interoperability for efficient model development.
the Intel AI Analytics Toolkit (AI Kit) can significantly benefit the water quality prediction project by providing tools and resources for efficient data processing, model training, deployment, and ongoing optimization. Its performance optimization capabilities are particularly relevant when working with large datasets and complex machine learning models, as is often the case in environmental monitoring and prediction tasks.

## Models 
The following models were employed to capture varying tendencies of the dataset. Each model brings something new to the table and its interesting to observe some models perform significantly better than others. This is due to the nature of the dataset.
•	**Neural Networks (NN)**
Neural Networks, often referred to as deep learning models, have gained prominence in machine learning due to their ability to handle complex, high-dimensional datasets effectively. They are a powerful choice for various tasks, including predicting water quality based on multiple water parameters.

•	**Logistic Regression**

Logistic Regression is often employed as a baseline model in machine learning projects, serving as a benchmark against which the performance of more complex models can be compared. It offers interpretable metrics like precision, recall, and F1-score, which are crucial for assessing a binary classification model's effectiveness.

•	**Decision Tree Classifier**

The Decision Tree Classifier is a versatile machine learning algorithm that can be used for both classification and regression tasks. In this analysis, we explore its application in predicting water quality suitability for consumption based on various water parameters.


•	**Random Forest Classifier**

Random Forest is a robust ensemble algorithm that combines multiple decision trees to improve predictive accuracy and reduce overfitting. It's a suitable choice for this task due to its ability to handle complex datasets with multiple features, making it well-suited for predicting water quality based on various water parameters.

•	**Voting Classifier**

The code introduces an ensemble modeling approach that combines the power of two machine learning algorithms, Decision Trees and Random Forests, in a Voting Classifier. This ensemble technique is employed to enhance the predictive accuracy and robustness of the model. The Decision Tree and Random Forest algorithms are chosen due to their individual strengths and complementarity in handling different aspects of the data.

•	**XGBoost**
XGBoost is a popular and powerful machine learning algorithm that is widely used for classification and regression tasks. It stands for eXtreme Gradient Boosting and is an implementation of gradient boosting machines. XGBoost is known for its speed and performance, as well as its ability to handle large datasets and high-dimensional feature spaces. It has been shown to achieve state-of-the-art results on a variety of machine learning tasks, making it a popular choice among data scientists and machine learning practitioners

•	**AdaBoost Classifier**

The AdaBoost Classifier is an ensemble machine learning algorithm known for its ability to improve the performance of weak classifiers. In this analysis, we explore its application in predicting water quality suitability for consumption based on various water parameters.

•	**Passive Aggressive Classifier**

The Passive Aggressive Classifier is a machine learning algorithm suited for binary classification tasks. In this code analysis, we explore its application in predicting water quality suitability for consumption based on various water parameters.

### Metric used for judging:

When judging different machine learning models for the specific task, several metrics are used to assess the performance. 

#### Classification Metrics:
**Accuracy:** 
It measures the proportion of correctly classified instances out of the total. It's suitable for balanced datasets.
**Precision:**
Also known as positive predictive value, it measures the proportion of true positive predictions out of all positive predictions. It's useful when false positives are costly.
**Recall (Sensitivity or True Positive Rate):**
It measures the proportion of true positive predictions out of all actual positives. It's useful when false negatives are costly.
**F1-Score:** 
The harmonic mean of precision and recall. It balances precision and recall and is useful when there's an imbalance between classes.
**ROC AUC (Receiver Operating Characteristic Area Under the Curve):** 
It measures the model's ability to distinguish between positive and negative classes. It's particularly useful when you want to evaluate the **trade-off between true positive rate and false positive rate across different thresholds.
**Precision-Recall Curve:**
It visualizes the trade-off between precision and recall at various thresholds. It's useful when class imbalance is significant.


| Model               | F1-Score|Precision| Recall  | Accuracy| ROC AUC |
|---------------------|---------|---------|---------|---------|---------|
| Neural Network      | 0.793   | 0.789   | 0.797   |         |         |
| Logistic Regression | 0.57    | 0.72    | 0.47    | 0.78    |         |
| Adaboost            | 0.76    | 0.82    | 0.71    | 0.87    |         |
| XGBoost             | 1.00    | 1.00    | 1.00    | 1.00    | 1.00    |
| PAC                 | 0.53    | 0.57    | 0.49    | 0.73    |         |
| Random Forest       | 0.86    | 0.77    | 0.98    | 0.90    |         |
| Decision Tree       | 1.00    | 1.00    | 1.00    | 1.00    | 1.00    |



#### In this table:
**F1-Score:** Measures the balance between precision and recall. Higher values indicate a better balance.

**Precision:** Indicates the ability of the model to make accurate positive predictions. Higher precision means fewer false positives.

**Recall:** Measures the model's ability to capture positive instances. Higher recall means fewer false negatives.

**Accuracy:** Overall model accuracy.

**ROC AUC:** Area Under the Receiver Operating Characteristic (ROC AUC) curve, which represents the model's ability to discriminate between positive and negative classes. A higher value indicates better discrimination.

### Based on these metrics, the XGBoost and Decision Tree models appear to perform exceptionally well, achieving perfect scores in many metrics.


In summary, the Intel OneAPI Toolkit offered a comprehensive suite of tools and libraries that were finely tuned for Intel hardware. This gave you a significant advantage during the hackathon by improving performance, enabling parallelism, and providing detailed insights into your code's efficiency. While sklearn is a valuable library for machine learning and data analysis, it may not offer the same level of hardware-specific optimizations and parallel computing capabilities that the Intel Toolkit provides, making it a powerful choice for high-performance computing and accelerated development in specific domains.
					



     
  
  
  
  

  

  

  
  





