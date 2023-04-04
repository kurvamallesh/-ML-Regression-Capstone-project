# -ML-Regression-Capstone-project-new

# Bike Sharing Demand Prediction(Regression)
Bike Sharing Demand Prediction

## EDA Conclusion

* Session are making huge impact on **Rented Bike Count** where in **summer** **(2283234)** there was very high count and in **Winter** **(487169)** very low

* We know there are **high** **Rented Bike Count**  in **Summer** but In **Holiday** peoples are like to book the bike in **Autumn** session more.So we can say Autumn session is best for Holiday.

* We found there some rowes that have **Humidity** as **0** so it is not possible so we need to check this.

* Less then **-10** **Temperature**(°C) making huge impacting on **Rented Bike Count**

* We suggest to the company please give **high prefrence** to **8pm**. Because in this time **Rented Bike Count** are very high.

* We can say there are **not much** bike ranted count after **Wind speed** **5(m/s)**

* We can say there are very less **Rented bike count** on greater then **5(mm)** **Rainfall**.

* Also we can see **Snowfall** directlly **impacting** on **Rented Bike Count**.

* According to bar plot we can say that **Rented Bike Count** is very high in **june** month.

##  **Conclusion for Model Training**

**Abut some Feature engineering:-**

* First we convert chatogorical values to num values.

* Converting date column dtype object to date.split **day of week**, **month** and **year** in three column

* Creating New feature **Week day** and **weekend**. And droping the days of week column from data and from categorical feature.

* Convert Hour column in three part Night, Noon, Evening, Morning For better predictation.

* Using correlation plot we find **"Dew point temperature(°C)"** variable is higlly correlated.

* Using VIF there is '**Dew point temperature(°C)'** is **multicollinearity**.So decide to drop Dew point temperature(°C).


**About models:-**

* Also using **Power Transformer** for scaling and transform it after train test split so we can aboide overfitting.

* Create a function for print the scores so we can use this function.

* Fist we use some **Linear Regression** and then use **Lasso** and **Ridge** with the help of **Hyperparameter Tuning**

* Using **PolynomialFeatures** with **Linear Regression**. but we did not get good scores.

* Then we use Tree Base Models because we know because **multicollinearty not** effect **tree base models**.So use we Random **Forest Regressor** and **Decision Tree**.

* Then we decide to use some boosting regression for better predictions. So we use **Gradient Boosting Regressor**, **Adaboost Boost Regressor**, **XGBoost Regression**. We got our best **rmse** score with Linear,	Lasso,	Ridge,	Polynomial. We got our best **Training_score** with Random_Forest. We got our best R2, Adjusted_R2 with Decision_Tree,	Random_Forest,	Bagging.d
