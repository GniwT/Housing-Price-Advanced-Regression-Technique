# House Prices Advanced Regression Techniques
## Machine Learning with Pipelines, Stacking, and Voting Regressor

In this project, I will cover the cycle of machine learning project with pipeline, blending the estimators with stacking and voting.

The dataset if from Kaggle Competition - House Prices Advanced Regression Techniques. I choose to extract the dataset with Kaggle API and run on colab because Colab is more stable than Kaggle notebook. The public scores I got from these project are around 0.14, which is quite satisfactory on housing price prediction.

The Lifecycle in a Data Science Projects:

* Data Analysis
* Feature Engineering
* Feature Selection
* Feature Engineering
* Model Building

Pipeline

Piple is used to connect multiple estimators in sequence. It is useful to machine learning by combining a sequence of steps during data-processing such as feature engineering, data-scaling and regression in one chain. One of the major benefits of the pipeline is to help avoid data leakage when applying the trained model from cross-validation onto the test data.

Data leakage in an important topic in machine learning. When data scientists prepare the trained model, we have to separate the train and the test data separately. We attain the best accuracy in the trained model, but the model could fail when deploying into production. If some of the data in the test data is shared to the training set, or vice versa, the results from the leaked models would give us the deceptive and even unrealistically 'good' predictions. The test data is the simulation of the production in reality, thus the information in test dataset is not allowed to be known in the training data. Most data leakage is cuased by unintentional mistakes made during data preprocessing and feature engineering.

Data leakage is a common problem not only in data science competitions, but also in real production. The companies may lose much money on failed business plans due to the overly optismistic predictions with data leakage. We can avoid data leakage by cross-validation and pipeline. Sci-kit learn offer some useful techquies to tackle data leakager. We will walk through it in this model.
