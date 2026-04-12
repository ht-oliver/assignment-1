# Homework 1 Task 3

---

Answer the following questions based on exercises from *An Introduction to Statistical Learning with Applications in Python*.

## Chapter 2.4 Exercises

---

### Exercise 1 (ISLP exercise 2)

Explain whether each scenario is a **classification or regression** problem, and indicate whether we are most interested in **inference or prediction**. Finally, provide **n** (size of observation dataset) and **p** (number of predictors).

**(a)**  We collect data on 200 protected marine reserves worldwide. For each reserve we record species richness, reserve size, years since establishment, enforcement budget, and proximity to human settlements. We are interested in understanding which factors affect species richness.

> This is a regression problem, and we're more interested in inference. The goal of this scenario is to get more information about the relationships between predictors and a numeric outcome (richness), which means that we'll want to see numerical relationship values that would come from a regression. Furthermore, we're interested in inference because we just want to see relationship metrics, we're not concerned with yielding values for predictions (yet). In this case, n = 200, p = 4.

---

**(b)** A conservation agency wants to know whether a proposed habitat corridor will successfully support wildlife movement or fail to do so. They collect data on 30 previously established corridors. For each corridor they have recorded whether wildlife movement was successful or unsuccessful, corridor width, length, surrounding land use type, and eight other variables.

> Given our outcome metric is categorical (successful/unsuccessful) this is a classification scenario. In this case, we are interested in predictions because the conservation agency is trying to find out what combinations of predictor metrics will produce "successful" results. For this scenario n = 30, p = 11.

---

**(c)** We are interested in predicting weekly average ground-level ozone concentration in a coastal city. We collect weekly data for all of 2019. For each week we record average ozone concentration, sea surface temperature, wind speed, solar radiation, and atmospheric

> Since we're looking for a numeric concentration, and we want to make predictions, this is regression problem that is interested in predictions. I think the list of predictors was cut off partially for this question, but I believe for this scenario n = 52 (weeks in 2019), and p = 4.

---

### Exercise 2 (ISLP exercise 5)

What are the advantages and disadvantages of a very flexible (versus a a less flexible) approach for regression? Under what circumstances might a more flexible approach be preferred to a less flexible approach? When might a less flexible approach be preferred?

> Very flexible approaches allow for us to account for more variables in our model, but they can also result in over-fitting, where our model becomes useful only for our training data and cannot be meaningfully extrapolated onto other scenarios. Flexible approaches are generally prefferred when you have more data, and are looking to make predictions. You would want a more flexible approach if there are multiple predictors that you expect to have dramatic impacts of similar magnitude on your outcome. For example, if you were trying to predict species presence in an environment where there are both dramatic weather changes AND a hunting season, you would want your model to be able to account of both, and the interaction between the two, rather than just be accounting for mortality. If you were trying to look at a predator/prey relationship in a protected habitat where weather is relatively consistent and species populations are primarily controlled by predator presence, you would probably want a more rigid model that has heavy dependence on predator presence.

---

### Exercise 3 (ISLP exercise 6)

Describe the differences between a **parametric** and a **non-parametric** statistical learning approach. What are the **advantages** of a parametric approach to regression or classification (as opposed to a non-parametric approach)? What are its **disadvantages**?

> A parametric approach assumes that there is an existing relationship between predictors and outcomes in a given model - which influences how models are designed. Non-parametric approaches to not assume any existing relationship, and models are designed to "search" for relationships. Parametric approaches allow for more rigidity in models, and can support more direct conclusions - but they can also be misleading in this way. Non-parametric methods are more flexible, but as we discussed earlier flexibility can open doors to avoidable error. Generally, parametric approaches are better for learning fundamentals of regression, but they can limit you in what relationships you're able to look at.