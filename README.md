# FashionImagesClassification
## Identify and Classify Fashion Images and Label correctly

## Jupyter Notebook

## DataSet
https://github.com/ravikduvvuri/PA3_ComparingClassifiers/blob/main/bank-additional-full.csv



## 1. Overview
In this practical application, my goal is to compare the performance of the classifiers we encountered in this section, namely K Nearest Neighbor, Logistic Regression, Decision Trees, and Support Vector Machines. We will utilize a dataset related to marketing bank products over the telephone. As a Data Scientist, my job is to train various classification models and score performance of each one and identify the best one for the given dataset problem **ie., has the client subscribed a term deposit? (binary: 'yes','no')**

## 2. Business Understanding
To gain a better understanding of the data, please read the information provided in the UCI link in the attached dataset, and examine the Materials and Methods section of the paper. **How many marketing campaigns does this data represent?**
  
   _**The dataset is the result of 17 marketing campaigns**_

## 3. Data Understanding
To understand the data, I did the following:

  ### 3.1 Initial steps done
    
    3.1.1 Imported relevant libraries 
    
    3.1.2 Read 'bank-additional-full.csv' into a pandas dataframe
    
    3.1.3 Displayed sample data using df.sample(10) to see what features are there in the dataset
    
    3.1.4 Gained some domain knowledge and checked data and possible relationships among them
  
  ### 3.2 Next steps done
  
    3.2.1 Using df.info() found the total features, size of the dataset and data types of features
    
    3.2.2 Checked for 'missing data'
    
    3.2.3 Searched for duplicate data
    
  ![Alt text](https://github.com/ravikduvvuri/PA3_ComparingClassifiers/blob/main/pa3_nulldata.jpeg)

## 4. Data Preparation

### 4.1 Pre-processing of data / Data cleanup
  Based on data analyis, I did the following:

    4.1.1 Data seems clean, so no extensive pre-processing was done

    4.1.2 Removed duplicate data
    
    4.1.3 Removed outliers data using Z_score
       
### 4.2 Plots of Clean data
  These plots provide the information about how clean data looks like from distribution perspective
  
    4.2.1 Box plots - Numeric data
    
    4.2.2 Bar Plots - Categorical data

![Alt text](https://github.com/ravikduvvuri/PA3_ComparingClassifiers/blob/main/Plots%20-%20Duration.jpeg)

![Alt text](https://github.com/ravikduvvuri/PA3_ComparingClassifiers/blob/main/Plots%20-%20Campaign.jpeg)

![Alt text](https://github.com/ravikduvvuri/PA3_ComparingClassifiers/blob/main/CPlots%20-%20Job.jpeg)

![Alt text](https://github.com/ravikduvvuri/PA3_ComparingClassifiers/blob/main/Cplots%20-%20y.jpeg)

![Alt text](https://github.com/ravikduvvuri/PA3_ComparingClassifiers/blob/main/ScatterPlot.jpeg)


## 5. Engineering Features

**5.1 Encoder, Column Transformation and data split:**

    5.1.1 Used Encoder and Column Transformation
    
    5.1.2 Initialized StandardScaler, OnehotEncoder, LabelEncoder
    
    5.1.3 Split data into Train/Test data

## 6. Models

**6.1 Base model**

    6.1.1 Built Baseline Accuracy

**6.2. Logistic Regression**
    
    6.2.1 Built Logistic Regression model and got train, test scores.
    
**6.3. KNN Model**
    
    6.3.1 Built KNN model and got train, test scores.

**6.4. Decision Tree Model**
    
    6.4.1 Built Decision Tree model and got train, test scores

**6.5. SVM Model**
    
    6.5.1 Built SVM model and got train, test scores

**6.6. Model Comparisions**
    
    6.6.1 Created a table with fit time, train, test accuracy data
    
![Alt text](https://github.com/ravikduvvuri/PA3_ComparingClassifiers/blob/main/Model%20scores%20comparision.jpeg)

## 7.Model Finetuning
    
    7.1.1 Did Hyperparameter tuning
    
    7.1.2 Performed GridSearch
    
    7.1.3 Built Confusion Matrix, Accuracy, Recall, Precision, F1Score
    
    7.1.4 Created a table with fit time, train, test accuracy data along with Confusion Matrix info
    
    7.1.5 Plotted the model comparision via histograms
    
    7.1.6 Plotted ROC-AUC
    
![Alt text](https://github.com/ravikduvvuri/PA3_ComparingClassifiers/blob/main/ConfusionMatrix.jpeg)

![Alt text](https://github.com/ravikduvvuri/PA3_ComparingClassifiers/blob/main/Improved%20model%20scores%20comparision.jpeg)

![Alt text](https://github.com/ravikduvvuri/PA3_ComparingClassifiers/blob/main/Model%20Comparision%20HistPlot.jpeg)

![Alt text](https://github.com/ravikduvvuri/PA3_ComparingClassifiers/blob/main/ROC%20Curve.jpeg)


**Based on models evaluation, The DecisionTree Model has shown good performance and better Recall, F1 Score, Train/Test accurancy and model fit time**
