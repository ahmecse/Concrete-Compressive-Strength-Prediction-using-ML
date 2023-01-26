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

## 3. Modelling and Evaluation

* Algorithms used
  * Linear regression
  * Lasso regression
  * Ridge regression
  * Decision Trees
  * Random Forests

* Metric - Since the target variable is a continuous variable, regression evaluation metric RMSE (Root Mean Squared Error) and R2 Score (Coefficient of Determination) have been used.

## 4. Results

#### Feature correlation
![Feature correlation](https://github.com/ahmecse/Concrete-Compressive-Strength-Prediction-using-ML/blob/0b8ffa87629dc7e972d10ce8b377fcee7c5cfa41/resources/1.png)
#### Feature importance
![Feature importance](https://github.com/ahmecse/Concrete-Compressive-Strength-Prediction-using-ML/blob/0b8ffa87629dc7e972d10ce8b377fcee7c5cfa41/resources/3.png)
#### Feature of the given data sets and the models 
![Feature importance](https://github.com/ahmecse/Concrete-Compressive-Strength-Prediction-using-ML/blob/9496ade498919091cf36a5b5812bed303da48c6a/resources/5.png)
#### Final Comparison
![Final Comparison](https://github.com/ahmecse/Concrete-Compressive-Strength-Prediction-using-ML/blob/0b8ffa87629dc7e972d10ce8b377fcee7c5cfa41/resources/4.png)


## 5. References
1. https://archive.ics.uci.edu/ml/datasets/Concrete+Compressive+Strength
