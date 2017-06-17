# Supervised Learning

+ Most common.
+ The program is “trained” on a pre-defined set of “training examples”, which then facilitate its ability to reach an accurate conclusion when given new data..
+ Supervised learning problems are categorized into "regression" and "classification" problems.

### collect training data --> train classifier --> make predictions 

# Classification 
Discrete valued output. We are trying to map input variables into discrete categories. When y can take on only a small number of discrete values (such as if, given the living area, we wanted to predict if a dwelling is a house or an apartment, say), we call it a classification problem. 
Example: Given a patient with a tumor, we have to predict whether the tumor is malignant or benign (0 no / 1 yes) 

# Regression
Predict continuous valued output. Meaning that we are trying to map input variables to some continuous function. When the target variable that we’re trying to predict is continuous we call the learning problem a regression problem. 

--example: Given a picture of a person, we have to predict their age on the basis of the given picture

# Measuring Performance


# Unsupervised Learning

+ The program is given a bunch of data and must find patterns and relationships therein.

Allows us to approach problems with little or no idea what our results should look like.
We can derive this structure by clustering the data based on relationships among the variables in the data.
With unsupervised learning there is no feedback based on the prediction results.
Clustering

Take a collection of 1,000,000 different genes, and find a way to automatically group these genes into groups that are somehow similar or related by different variables, such as lifespan, location, roles, and so on.

Non-clustering

The "Cocktail Party Algorithm", allows you to find structure in a chaotic environment. (i.e. identifying individual voices and music from a mesh of sounds at a cocktail party).

Dimensionality Reduction

Density Estimation
