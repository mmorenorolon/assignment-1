# Homework 1 Task 3

---

Answer the following questions based on exercises from *An Introduction to Statistical Learning with Applications in Python*.

## Chapter 2.4 Exercises

---

### Exercise 1 (ISLP exercise 2)

Explain whether each scenario is a **classification or regression** problem, and indicate whether we are most interested in **inference or prediction**. Finally, provide **n** (size of observation dataset) and **p** (number of predictors).

**(a)**  We collect data on 200 protected marine reserves worldwide. For each reserve we record species richness, reserve size, years since establishment, enforcement budget, and proximity to human settlements. We are interested in understanding which factors affect species richness.

> The dataset contains information on 200 marine reserves, therefore the size of the observation dataset **n** is 200. For each reserve they recorded 4 predictors (reserve size, years since establishment, enforcement budget, and proximity to human settlements), so **p**  is 4. The scenario can be classified a regression problem, since species richness is a quantitative response variable. The goal is inference, as we are trying to understand the how the stated predictors are associated with species richness, not necessarily trying to predict the species richness from the predictors.   

---

**(b)** A conservation agency wants to know whether a proposed habitat corridor will successfully support wildlife movement or fail to do so. They collect data on 30 previously established corridors. For each corridor they have recorded whether wildlife movement was successful or unsuccessful, corridor width, length, surrounding land use type, and eight other variables.

> This is a classification problem because the response variable, wildlife movement success, is qualitative and is taking values such as successful or unsuccessful. The goal is prediction, as the agency is interested in using the predictors to accurately classify whether a proposed corridor will be successful, rather than understanding the relationship between the predictors and the response. The dataset contains information on 30 corridors, so **n** is 30. There are 11 predictor variables (corridor width, length, surrounding land use type, and eight additional variables), so **p** is 11.

---

**(c)** We are interested in predicting weekly average ground-level ozone concentration in a coastal city. We collect weekly data for all of 2019. For each week we record average ozone concentration, sea surface temperature, wind speed, solar radiation, and atmospheric 

> This is a regression problem because the response variable, weekly average ozone concentration, is quantitative. The goal is prediction, as we are interested in using the predictor variables to accurately estimate ozone levels rather than understanding their individual effects. The data are collected weekly for one year, so **n** is 52. There are four predictor variables (sea surface temperature, wind speed, solar radiation, and atmospheric conditions), so **p** is 4.

---

### Exercise 2 (ISLP exercise 5)

What are the advantages and disadvantages of a very flexible (versus a a less flexible) approach for regression? Under what circumstances might a more flexible approach be preferred to a less flexible approach? When might a less flexible approach be preferred?

> A more flexible regression approach allows the model to better capture complex, non-linear relationships between predictors and the response, which can lead to improved predictive accuracy when the true relationship is complicated. However, flexible models are more prone to overfitting, meaning they may fit the training data very closely but perform poorly on new data. They are also less interpretable, as the relationship between predictors and the response can become difficult to understand. In contrast, less flexible approaches produce simpler models that are easier to interpret and are less likely to overfit, but they may underfit the data if the true relationship is complex. A more flexible approach is preferred when the primary goal is prediction and there is reason to believe the underlying relationship is complex, especially when a large amount of data is available. A less flexible approach is preferred when inference is the goal, since simpler models make it easier to understand how each predictor is associated with the response or when the sample size is small and overfitting is a concern.

---

### Exercise 3 (ISLP exercise 6)

Describe the differences between a **parametric** and a **non-parametric** statistical learning approach. What are the **advantages** of a parametric approach to regression or classification (as opposed to a non-parametric approach)? What are its **disadvantages**?

> A parametric approach assumes a specific functional form for f, such as a linear relationship, and then uses the training data to estimate a set of parameters that define that function. In contrast, a non-parametric approach does not assume a particular shape for f, and instead seeks to estimate it more flexibly so that it closely follows the observed data. The main advantage of a parametric approach is that it simplifies the problem by reducing it to estimating a limited number of parameters, which makes it computationally efficient and requires less data. Parametric models are also generally easier to interpret, especially when the goal is inference. However, a key disadvantage is that the assumed functional form may not match the true underlying relationship. If this assumption is incorrect, the model can perform poorly due to high bias. While more flexible parametric models can be used to better approximate complex relationships, they may require estimating more parameters and can lead to overfitting, especially when the sample size is small. 