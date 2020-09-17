# Predicting Student Exam Results

For years, students have been using their predicted grades in an effort to monitor their progress throughout their chosen subjects. More recently, as a result of the Covid-19 pandemic, predicted grades have been used by exam boards, particularly within the UK, as a student's final grade. As a result, the accurate prediction of these grades has grown significantly more important.

There were two main aims of this project. The first was to further practice the skills and techniques I had learned as a result of completing Jose Portilla's "Python for Data Science Bootcamp" course on [Udemy](https://www.udemy.com/course/python-for-data-science-and-machine-learning-bootcamp/learn/lecture/17739846?start=0). The second aim was to create models that would accurately predict the score that a student would achieve based on features such as race and the level of education reached by their parents.

## Table of Contents

* [Technologies](#technologies)
* [Exploratory Data Analysis](#exploratory_data_analysis)
* [Data Preprocessing](#data_preprocessing)
* [Model Building](#model_building)
* [Model Performance](#model_performance)

## Technologies

This project was created using a Jupyter Notebook with the following package versions installed:

* Python: 3.7.7
* Imbalanced-Learn: 0.7.0
* Numpy: 1.19.1
* Pandas: 1.1.0
* Seaborn: 0.10.1
* Scikit-Learn: 0.23.1
* Matplotlib: 3.2.2
* Tensorflow: 2.1.0
* Keras: 2.3.1

## Exploratory Data Analysis

I checked the distribution of the test results and the relationships between each of the 3 test scores pairwise. I llooked at the value counts for the various catergorical variables. I analysed the effect of each independent variable on the test scores achieved in turn to determine any underlying relatioships within the data. I explored the relationships between the independent variables. Below are some of the highlights of the EDA.

![alt text](https://github.com/sykes14596/Student_Exam_Results/blob/master/Images/test_scores_pairplot.png "Test Scores Pairplot")
![alt text](https://github.com/sykes14596/Student_Exam_Results/blob/master/Images/race_v_scores_boxplot.png "Race v Scores Boxplot")
![alt text](https://github.com/sykes14596/Student_Exam_Results/blob/master/Images/parent_education_countplot.png "Parental Education Countplot")

## Data Preprocessing

I checked for outliers visually through the use of box plots. I thought of several possible situations that could be considered to be outliers and investigated the students that fell within each of these scenarios. I also made use of the interquartile range method and developed a function that looked for test scores that fell outside of the range [LQ - (1.5 x IQR), UQ + (1.5 x IQR)]. Finally, I converted each of the categorical variables into numerical features thorugh the use of Label Encoding and Dummy Variables.

## Model Building

In total, I attempted to build models to solve three different problems. These problems were:

* Predicting a students' average score - this made the problem into a regression problem.
* Predicting the score obtained in each of the 3 tests, converting the problem into a Multi Target Regression problem
* Predicting the grade achieved by each student, making the problem a multi-class classification problem. This problem also required the use of the SMOTE technique to create a balanced dataset.

In the first two problems, I implemented a linear regression model and a deep learning model. Despite a deep learning model not being appropriate for this problem, I chose to implement one in order to practice writing the code required. In the final problem, I implented 3 different models. These models were:

* Logistic Regression,
* K Nearest Neighbors,
* Random Forest Classifier.

## Model Performance

### Problem 1

In this problem, the mean absolute error was used to evaluate model performance. Full results are shown below.

* Linear Regression MAE: 10.1
* Deep Learning MAE: 10.7

### Problem 2

* Multi Target Linear Regression MAE: 10.5
* Multi Target Deep Learning MAE: 11.1

### Problem 3

In this problem, the accuracy of each model was analysed. Full results shown below.

* Logistic Regression: 31%
* K Nearest Neighbors: 39%
* Random Forest: 40%

Despite the poor performance of the models, this project enabled me to practice my skills and create inventive ways of looking at the problem. 