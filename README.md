# Salary-Prediction

# Introduction
This project employed three machine learning algorithms (i.e. **Naïve Bayes, K-Nearest Neighbors, and Random Forest**) to predict job salary based on role and requirements. The training set includes 8,000 job descriptions labelled with salary and 5,902 unlabeled descriptions. The development set for validation purpose has 1,737 job descriptions with target labels, and the test set has 1,738 unlabeled job descriptions. This project used the TFIDF and Embedding of job descriptions to make prediction. The objective is to select suitable models following data pre-processing, hyperparameter tuning, and performance metrics interpretation and comparison. This project also attempted to utilize unlabeled data to train models and explored whether it improved performance.

# Method
This project applied four types of input features to make predictions. Firstly, TFIDF and Embedding are the two types of input features. Alternatively, the project incorporated the two traits into one predictive feature. In addition, the project also standardized TFIDF and Embedding values and combined them to generate the fourth type of input feature.
In this project, DummyClassifier is used as the baseline model which predicts the labels of instances randomly and uniformly. Since the target of this project is to predict the correct job salary category, accuracy is used as the primary evaluation metric. The algorithms selected in this project are **Multinomial Naïve Bayes, K-Nearest Neighbors, and Random Forest**. For hyperparameter tuning, the project conducted a **5-fold cross validation** on the training set by using the **GridSearchCV** function in scikit-learn library. After obtaining the optimal parameters, the models would be evaluated on the validation set. The models with the highest validation accuracy within each algorithm would then be used to examine the effect of utilizing unlabeled data. The project implemented Semi-Supervised Learning via the **SelfTrainingClassifier** function in scikit-learn library. The process started by adding 1,000 unlabeled data to the pool, then increase by 500 with each subsequent iteration. The project also explored various **threshold** (prediction probability) and **k_best** (k highest confidence) values to determine which yields the best results. The flow chart of this project is presented below.
![flow chart](https://github.com/W-Hsieh/Salary-Prediction/assets/142127312/31c6d781-5405-4b44-bdfb-f18eb4d0af60)

# Results and Discussion

# Conclusion
