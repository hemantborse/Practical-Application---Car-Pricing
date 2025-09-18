# Practical-Application---Car-Pricing

**Problem statemant**

Analyse a dataset from Kaggle/ sub dataset of used cars which contains different features such as Year,odometer,cylinders,price etc.
Apply CRISP-DM process to  understand what factors make a car more or less expensive , result will be used to provide clear recommendations to our client—a used car dealership—as to what consumers value in a used car.

**Notebook code :**

https://github.com/hemantborse/Practical-Application---Car-Pricing/blob/main/Car_price.ipynb

**Observations on visual plots :**


**1.	From 2015 to 2020 there are some outliers, for example with ford where some prices are out of range.**
<img width="1457" height="525" alt="newplot (15)" src="https://github.com/user-attachments/assets/d128c8e5-47dc-4508-9c5c-3936dee17800" />



**2.	Cylinder 3 and 12 capacity cylinder cars are the least in number in dataset whereas more data available for 4,6- and 8-cylinder capacity cars.**

<img width="1457" height="525" alt="newplot (14)" src="https://github.com/user-attachments/assets/2a830979-e876-4ec3-9c25-a006e3343a38" />

<img width="1457" height="525" alt="newplot (10)" src="https://github.com/user-attachments/assets/a14a490e-a92e-45ae-af2a-5c38e3b680c2" />


3.	Most cars are in 10K to 15K range.
4.	Most cars are from 2010 to 2015

<img width="637" height="528" alt="image" src="https://github.com/user-attachments/assets/bee9aa2b-80db-40e0-8837-0a08fc6d5563" />

5.	Correlation Heatmap shows Odometer has negative correlation with price , means odometer goes higher price is lower hence it is an important factor to consider in this assignment
6.	Positive correlation between year and price also shows as year increase (newer cars), price goes up -another important factor to consider while training the model.
7.	Positive correlation in cylinders and price shows higher the cylinders’ value, higher is the price.


**Observations Liner Regression:**
1.	LinerRegression on different features shows different results.
2.	having only year and price combination OR year, odometer and price show similar MSE results.
3.	Once we consider cylinders feature with year, odometer and price, it brings MSE down to smaller value when add with year and odometer.
4.	The least MSE is seen when year and cylinder considered and price and prediction Vs Actual Sales Value are very close, hence this seems to be the most suitable model, at least for now.
5.	We, however, need to be careful how effective the least MSE combination would be in real world data, we must choose a model which can predict most accurately in real world scenarios.


**Observation** Low-degree polynomials (e.g., degree in this case 1)  -  A low-degree polynomial, is a simple model with low variance. Because it is not very flexible, it produces a very similar fit even with slightly different training data. However, if the true relationship is not linear, **this model will have high bias, resulting in large, systematic errors.**


**Observation Lasso Regression** train and test MSE has big deviation ,** LASSO might not be best model for this usecase**

**Conclusion - LinerRegression model giving accurate results hence is choice of model to be used for this usecase.**
