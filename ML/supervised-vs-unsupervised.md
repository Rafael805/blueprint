# Supervised Learning

+ Most common.
+ The program is “trained” on a pre-defined set of “training examples”, which then facilitate its ability to reach an accurate conclusion when given new data..
+ Supervised learning problems are categorized into "regression" and "classification" problems.

In **supervised learning**, the training data you feed to the algorithm includes the desired solutions, called **labels**. A typical supervised learning task is **classification**. Another typical task is to predict a **target** numeric value, such as the price of a car given a set of **features**(mileage, age, brand, etc.) called **predictors**. This sort of task is called **regression**.

### collect training data --> train classifier --> make predictions 

Important supervised learning algorithms: 
+ k-Nearest Neighbors
+ Linear Regression
+ Support Vector Machines (SVM)
+ Decision Trees and Random Forests 
+ Neural Networks 

# Classification 
Discrete valued output. We are trying to map input variables into discrete categories. When you can take on only a small number of discrete values (such as if, given the living area, we wanted to predict if a dwelling is a house or an apartment, say), we call it a classification problem.   

--example: Given a patient with a tumor, we have to predict whether the tumor is malignant or benign (0 no / 1 yes) 

# Regression
Predict continuous valued output. Meaning that we are trying to map input variables to some continuous function. When the target variable that we’re trying to predict is continuous we call the learning problem a regression problem. 

--example: Given a picture of a person, we have to predict their age on the basis of the given picture

# Unsupervised Learning

+ The program is given a bunch of data and must find patterns and relationships therein.

In **unsupervised learning** the training data is unlabeled. The system tries to learn without a teacher. It allows us to approach problems with little or no idea what our results should look like. We can derive this structure by clustering the data based on relationships among the variables in the data. With unsupervised learning there is no feedback based on the prediction results.

Important unsupervised learning algorithms: 
+ Clustering 
   + k-Means
   + Hierarchical Cluster Analysis (HCA)
   + Expectation Maximization
+ Visualization and dimensionality reduction
   + Principal Component Analysis (PCA)
   + Kernel PCA
   + Locally-Linear Embedding (LLE)
   + t-distributed Stochastic Neighbor Embedding (t-SNE)
+ Association rule learning 
   + Apriori 
   + Eclat

# Clustering

Take a collection of 1,000,000 different genes, and find a way to automatically group these genes into groups that are somehow similar or related by different variables, such as lifespan, location, roles, and so on.

# Non-clustering

The "Cocktail Party Algorithm", allows you to find structure in a chaotic environment. (i.e. identifying individual voices and music from a mesh of sounds at a cocktail party).

# Visualization
You feed them a lot of complex and unlabeled data, and they output a 2D or 3D representation of your data that can eassily be plotted.

# Dimensionality Reduction
The goal is to simplify the data without losing too much information. One way to do this is to merge several correlated features into one. 

# Association rule learning
The goal is to dig into latge amounts of data and discover interesting relations betweet attributes. 
