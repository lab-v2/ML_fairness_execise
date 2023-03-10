# ML_fairness_execise
This exercise is developed as part of course CSE-475 Found of Machine Learning to understand different fairness and biasness metrics.We all know that there's a huge real time application of AI and ML starting from simple stock prediction to complicated self driving cars, but with the increased use of AI and ML came the question of how fair and unbiased algorithms are the these algorithms. Correctional Offender Management Profiling for Alternative Sanctions(COMPAS) which can be considered the first and most popular case of development of biased algorithms in ML, a company developed a commercial algorithm used by judges and parole officers for scoring criminal defendant’s likelihood of reoffending (recidivism), though this software initially garnished a lot of popularity soon has to be shutdown when it's noticed it generally favors white defendants and is against black defendants. The reason why this issue occured despite not collecting the race data of the defendants is because of a question "Do you have a immediate member or a member in friends family who are convicted" which is a case of data to algorithm bias. This is the reason why we introduced Fairness and Biasness module to our course different from traditional courses which generally concentrates on ML algorithms like supervised, unsupervised learning Neural Networks etc.In order to make students understand the practical application of Fairness and Biasness we introduced a lab exercise. The goal of this exercise is to help you understand how aderversial debiasing helps in reducing the bias. We will be making use of package called aif360 which is been developed by IBM, you can find the package details and demo [here](https://aif360.mybluemix.net/). The readme file contains details on how to install the package and instructions to complete the exercise.
# Installation
 ## Linux
In order to install this package for linux we need to run following commands
  * apt-get install -y r-base
  * apt-get install -y python3-cffi
  * apt-get install -y python3-tk
  * pip install aif360[all]
 ## Windows
In order to install this package for windows we need to run following commands
  * Install r base from [here](https://cran.r-project.org/bin/windows/base/).
  * pip install aif360[all]
  * pip install pycario
# Exercise
The goal of this exercise is to show difference between classification metrics before and after adversarial debiasing.You should be able to download the fairness.py file for the template and use functions from [docs](https://aif360.readthedocs.io/en/stable/index.html#) to complete the exercise.The data we will be using for this exercise is the adult dataset from the UCI [repository](https://archive.ics.uci.edu/ml/machine-learning-databases/adult/) and copy paste the downloaded files to raw/data/adult folder present in aif360 package.You can also find further instructions in the fairness.py. Once completed you should be able to see the difference between classification metrics
 ## Steps
 * Load all necessary packages
 * Get the dataset and split into train and test
 * You need to create two different Adverarial models one with debiasing other without debiasing
 * Use ClassificationMetric from metrics module to get all the classification metric for the predicted and original test data
 * Print classification accuracy, balanced classification accuracy, equal opportunity difference for both models to compare the difference

