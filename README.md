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

