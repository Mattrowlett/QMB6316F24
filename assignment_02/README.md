# Assignment 2

Complete the exercise described in the pdf above and enter your answers in 
the spaces below.

## Running the Script as Given

Run the entire script and compare 
the output from ```summary(lm_full_model)```, 
which includes all variables, 
with that from ```summary(lm_no_damage)```, 
which omits the damage indicator. 
If there are no cars with damage in your simulation, 
run the script again to take another draw.


a. Copy and paste the regression model estimates after the commands
```summary(lm_full_model)``` and ```summary(lm_no_damage)```. 

```
Call:
lm(formula = car_price ~ mileage + accident + damage, data = car_data)

Residuals:
   Min     1Q Median     3Q    Max 
 -9570  -2820    282   2288  10194 

Coefficients:
              Estimate Std. Error t value Pr(>|t|)    
(Intercept)  4.779e+04  2.113e+03  22.621  < 2e-16 ***
mileage     -1.716e-01  4.276e-02  -4.013 0.000119 ***
accident    -4.551e+03  8.397e+02  -5.420 4.43e-07 ***
damage      -2.391e+04  4.163e+03  -5.743 1.09e-07 ***
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 4082 on 96 degrees of freedom
Multiple R-squared:  0.4961,	Adjusted R-squared:  0.4804 
F-statistic: 31.51 on 3 and 96 DF,  p-value: 2.887e-14


Call:
lm(formula = car_price ~ mileage + accident, data = car_data)

Residuals:
     Min       1Q   Median       3Q      Max 
-22993.2  -2483.5    301.9   2650.7  10651.8 

Coefficients:
              Estimate Std. Error t value Pr(>|t|)    
(Intercept)  4.915e+04  2.420e+03  20.308  < 2e-16 ***
mileage     -2.002e-01  4.897e-02  -4.087 9.00e-05 ***
accident    -5.136e+03  9.612e+02  -5.343 6.04e-07 ***
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 4708 on 97 degrees of freedom
Multiple R-squared:  0.323,	Adjusted R-squared:  0.309 
F-statistic: 23.14 on 2 and 97 DF,  p-value: 6.072e-09


```

b. Compare the estimated coefficient for ```ACCIDENT``` 
with and without the damage variable. 
How does this relate to the coefficient for ```DAMAGE```?

```
Type your response here.
```


c. Compare the values of 
```Multiple R-squared``` and ```Adjusted R-squared``` for the two models. 
Which model do you recommend (pretending that you don't know the true model)? 

```
Type your response here.
```




## Running the Script after Modification


d. Copy and paste the new regression model estimates after the commands
```summary(lm_full_model)``` and ```summary(lm_no_damage)```. 

```
beta_0          <-   50000     # Intercept
> beta_mileage    <- -  0.20     # Slope coefficient for mileage
> beta_accident   <- -  5000     # Slope coefficient for accident
> # beta_damage     <- - 20000     # Slope coefficient for damage
>  beta_damage     <-       0   # Alternate Slope coefficient for damage
> 
> # Distribution of mileage.
> avg_mileage <- 50000
> sd_mileage  <- 10000
> 
> # Fraction of dataset in an accident.
> pct_accident <- 0.4
> 
> # Frequency of damages (only after an accident).
> prob_damage <- 0.10
> 
> # Additional terms:
> sigma_2 <- 4000    # Variance of error term
> num_obs <- 100      # Number of observations in datasetbeta_0          <-   50000     # Intercept
> beta_mileage    <- -  0.20     # Slope coefficient for mileage
> beta_accident   <- -  5000     # Slope coefficient for accident
> # beta_damage     <- - 20000     # Slope coefficient for damage
>  beta_damage     <-       0   # Alternate Slope coefficient for damage
> 
> # Distribution of mileage.
> avg_mileage <- 50000
> sd_mileage  <- 10000
> 
> # Fraction of dataset in an accident.
> pct_accident <- 0.4
> 
> # Frequency of damages (only after an accident).
> prob_damage <- 0.10
> 
> # Additional terms:
> sigma_2 <- 4000    # Variance of error term
> num_obs <- 100      # Number of observations in dataset

Call:
lm(formula = car_price ~ mileage + accident, data = car_data)

Residuals:
     Min       1Q   Median       3Q      Max 
-22993.2  -2483.5    301.9   2650.7  10651.8 

Coefficients:
              Estimate Std. Error t value Pr(>|t|)    
(Intercept)  4.915e+04  2.420e+03  20.308  < 2e-16 ***
mileage     -2.002e-01  4.897e-02  -4.087 9.00e-05 ***
accident    -5.136e+03  9.612e+02  -5.343 6.04e-07 ***
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 4708 on 97 degrees of freedom
Multiple R-squared:  0.323,	Adjusted R-squared:  0.309 
F-statistic: 23.14 on 2 and 97 DF,  p-value: 6.072e-09
Copy your results here.
```


e. For this new set of regressions, compare the estimated coefficient 
for ```ACCIDENT``` with and without the damage variable. 
How does this relate to the new coefficient for ```DAMAGE```?

```
Type your response here.
```


f. Compare the values of 
```Multiple R-squared``` and ```Adjusted R-squared``` for the two models. 
Now which model do you recommend (pretending that you don't know the true model)? 

```
Type your response here.
```

