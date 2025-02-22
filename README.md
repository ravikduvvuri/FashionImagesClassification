# FashionImagesClassification
## Identify and Classify Fashion Images and Label correctly

## Jupyter Notebook

## DataSet

  ## Label data:
  https://github.com/ravikduvvuri/FashionImagesClassification/blob/main/styles.csv

  ## Images data:
  https://www.kaggle.com/datasets/paramaggarwal/fashion-product-images-dataset/data


## 1. Overview and Business Understanding
For a fashion retailer or manufacturer, identifying and entering product attributes into a system is a tedious job; if we have a model that can classify images and get attributes, it is a great help for them and it can also enhance master product data store with less effort. In this project, my goal is explore various models and create a better model to classify images and update label attributes into a dataframe. To Train and Test the models, I leveraged the fashionProductImages Dataset from Kaggle.

## 2. Data Understanding
To understand the data, I did the following:

  ### 3.1 Initial steps done
    
    3.1.1 Imported relevant libraries and packages
    
    3.1.2 Read 'styles.csv' into a pandas dataframe and Loaded product images into /images folder
    
    3.1.3 Displayed sample data using df.sample(10) to see what features are there in the dataset
    
    3.1.4 Gained some domain knowledge and checked data and possible relationships among them
  
  ### 3.2 Next steps done
  
    3.2.1 Using df.info() found the total features, size of the dataset and data types of features
    
    3.2.2 Checked for 'missing data'
    
    3.2.3 Searched for duplicate data
    
  ![Alt text](https://github.com/ravikduvvuri/FashionImagesClassification/blob/main/MissingDataStats.png)

## 4. Data Preparation

### 4.1 Data cleanup
  Based on data analyis, I did the following:

    4.1.1 Data seems clean, so no extensive pre-processing was done

    4.1.2 No duplicate found
    
    4.1.3 Removed missing data rows as they are not needed for images classification
       
### 4.2 EDA on Styles data
  These plots provide the information about how clean data looks like from distribution perspective
  
    4.2.1 Colour distribution by Gender
    
    4.2.2 Colour distribution by Master Category

    4.2.3 Colour distribution by usage

![Alt text](https://github.com/ravikduvvuri/FashionImagesClassification/blob/main/Color%20Distribution-Gender.png)

![Alt text](https://github.com/ravikduvvuri/FashionImagesClassification/blob/main/Color%20Distribution-MasterCategory.png)

![Alt text](https://github.com/ravikduvvuri/FashionImagesClassification/blob/main/Color%20Distribution-Usage.png)

### 4.3 EDA on Images data
  These plots provide the information about how clean data looks like from distribution perspective
  
    4.3.1 Display sample pictures
    
    4.3.2 Colour distribution of a sample image

![Alt text](https://github.com/ravikduvvuri/FashionImagesClassification/blob/main/SampleImages.png)

![Alt text](https://github.com/ravikduvvuri/FashionImagesClassification/blob/main/Color%20Distribution-SampleImage.png)

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
