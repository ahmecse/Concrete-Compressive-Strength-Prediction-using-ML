
# Concrete-compressive-strength

## Concrete Compressive Strength Prediction using Machine Learning

Concrete is one of the most important materials in Civil Engineering. Knowing the compressive strength of concrete is very important when constructing a building or a bridge. The Compressive Strength of Concrete is a highly nonlinear function of ingredients used in making it and their characteristics. Thus, using Machine Learning to predict the Strength could be useful in generating a combination of ingredients which result in high Strength.

Please refer [*GE22M009_concrete_comprehensive_strength_with_linear_regres.ipynb*](https://github.com/ahmecse/Concrete-Compressive-Strength-Prediction-using-ML/blob/0b8ffa87629dc7e972d10ce8b377fcee7c5cfa41/GE22M009_concrete_comprehensive_strength_with_linear_regres.ipynb) for code.

## 1. Problem Statement
Predicting Compressive Strength of Concrete given its age and quantitative measurements of ingredients.

## 2. Data Description

Data is obtained from UCI Machine Learning Repository.
https://archive.ics.uci.edu/ml/datasets/Concrete+Compressive+Strength

* Number of instances - 1030
* Number of Attributes - 9
  * Attribute breakdown - 8 quantitative inputs, 1 quantitative output

#### Attribute information
##### Inputs
* Cement
* Blast Furnace Slag
* Fly Ash
* Water
* Superplasticizer
* Coarse Aggregate
* Fine Aggregate

All above features measured in kg/$m^3$

* Age (in days)

##### Output
* Concrete Compressive Strength (Mpa)

## 2.Approach:
1. Loading the dataset using Pandas and performed basic checks like the data type of each column and having any missing values.
2. Performed Exploratory data analysis:
    * First viewed the distribution of the target feature, "Concrete compressive strength", which was in Normal distribution with a very little right skewness.
    * Visualized each predictor or independent feature with the target feature and found that there's a direct proportionality between cement and the target feature while there's an inverse proportionality between water and the target feature.
    * To get even more better insights, plotted both Pearson and Spearman correlations, which showed the same results as above.
    * Checked for the presence of outliers in all the columns and found that the column 'age' is having more no. of outliers. Removed outliers using IQR technique, in which I considered both including and excluding the lower and upper limits into two separate dataframes and merged both into a single dataframe. This has increased the data size so that a Machine learning model can be trained efficiently.

3. Experimenting with Linear regression algorithm:
First, with Linear regression 2nd, Lasso Regression and 3rd with Ridge Regression.

4. Experimenting with diffrent Optimazation Algorithms:

## 4.Optimazation Algorithms - Python and Pytorch Implementations

This repository contains Python and Pytorch implementations of various gradient descent algorithms. The purpose of this repository is to demonstrate how to implement various gradient descent algorithms using Python and Pytorch, and to compare their performances in terms of various evaluation metrics.

Please refer [*3-Gradient_Descent_And_ its_variants.ipynb*](https://github.com/ahmecse/Concrete-Compressive-Strength-Prediction-using-ML/blob/c187f01ac807c78874d25b06704eca490862f2ad/3-Gradient_Descent_And_%20its_variants.ipynb) for code.

* ## Batch Gradient Descent:
  * Batch gradient descent is an optimization algorithm used to minimize a cost function by iteratively adjusting the model parameters in the direction of steepest descent. The following implementations of batch gradient descent are available in this repository:

    * Batch Gradient Descent without Input Data Normalization (Python)
    * Batch Gradient Descent with Input Data Normalization (Python)
    * Batch Gradient Descent without Input Data Normalization (Pytorch)
    * Batch Gradient Descent with Input data normalization (Pytorch)
* ### Metrics Comparison
![Matrics Comparison](https://github.com/ahmecse/Concrete-Compressive-Strength-Prediction-using-ML/blob/7432b7f6b4e4ad6b58bfa9937f5fbbea8cf91204/resources/bgd.png)

* ## Stochastic Gradient Descent
  * Stochastic gradient descent is an optimization algorithm used to minimize a cost function by iteratively adjusting the model parameters based on the gradient of the cost function computed using a single training example at a time. The following implementations of stochastic gradient descent are available in this repository:

    * Stochastic Gradient Descent with Input Data Normalization (Python)
    * Stochastic Gradient Descent without Input Data Normalization (Python)
    * Stochastic Gradient Descent without Input Data Normalization (Pytorch)
    * Stochastic Gradient Descent with Input data normalization (Pytorch)
* ### Metrics Comparison
![Matrics Comparision](https://github.com/ahmecse/Concrete-Compressive-Strength-Prediction-using-ML/blob/4eacc0bbe0646a66838692637f7c27abb0c46251/resources/sgd.png)
* ## Mini-Batch Gradient Descent
  * Mini-batch gradient descent is an optimization algorithm used to minimize a cost function by iteratively adjusting the model parameters based on the gradient of the cost function computed using a subset of the training data. The following implementations of mini-batch gradient descent are available.
    * Mini-Batch Gradient Descent (Python)
    * Mini-Batch Gradient Descent (Pytorch)
 * Metrics Comparison
![Metrics Comparison](https://github.com/ahmecse/Concrete-Compressive-Strength-Prediction-using-ML/blob/c187f01ac807c78874d25b06704eca490862f2ad/resources/mbgd.png)
* ## Gradient Descent with Momentum
  * Gradient descent with momentum is a variant of gradient descent that uses a momentum term to accelerate the convergence of the optimization algorithm. The following implementations of gradient descent with momentum are available in this repository:

    * Gradient Descent with Momentum (Python)
    * Gradient Descent with momentum (Pytorch)
* ### Metrics Comparison
![Metrics Comparison](https://github.com/ahmecse/Concrete-Compressive-Strength-Prediction-using-ML/blob/206ae285a93f18f34e6cdf0164dcd698a822d85d/resources/bgdm.png)
* ## Nesterov Accelerated Gradient Descent
  * Nesterov accelerated gradient descent is a variant of gradient descent that uses a modified update rule to accelerate the convergence of the optimization algorithm. The following implementations of Nesterov accelerated gradient descent are available in this repository:

    * Nesterov Accelerated Gradient Descent (Python)
    * Nesterov Accelerated Gradient Descent (Pytorch)
* ### Metrics Comparison
![Matrics Comparison](https://github.com/ahmecse/Concrete-Compressive-Strength-Prediction-using-ML/blob/46c28d9fa9bdf969655d02891ac05233820f085e/resources/bgdn.png)


## 5. Results

#### Feature correlation
![Feature correlation](https://github.com/ahmecse/Concrete-Compressive-Strength-Prediction-using-ML/blob/0b8ffa87629dc7e972d10ce8b377fcee7c5cfa41/resources/1.png)
#### Feature importance
![Feature importance](https://github.com/ahmecse/Concrete-Compressive-Strength-Prediction-using-ML/blob/0b8ffa87629dc7e972d10ce8b377fcee7c5cfa41/resources/3.png)
#### Feature of the given data sets and the models 
![Feature importance](https://github.com/ahmecse/Concrete-Compressive-Strength-Prediction-using-ML/blob/9496ade498919091cf36a5b5812bed303da48c6a/resources/5.png)
#### Final Comparison
![Final Comparison](https://github.com/ahmecse/Concrete-Compressive-Strength-Prediction-using-ML/blob/09f796711a13ff163c652022b7bbf7043c25d503/resources/finallr.png)


## 5. References
1. https://archive.ics.uci.edu/ml/datasets/Concrete+Compressive+Strength
