# What is Machine Learning (ML)?  

Machine learning is used for a variety of things such as image and voice recognition, spam detection, fraud detection, stock market, teaching a computer how to play chess, and of course, self-driving cars. One of the main differences from humans and computers is that humans learn from past experience, whereas computers need to be programmed. Can we get computers to learn from experience too? **YES**, we can. That is exactly what machine learning is. Teaching computers to learn to perform tasks form past experiences. For computers, past experiences are just recorded as data. The ultimate goal of Machine Learning is to have data models that can learn and improve over time. In essence machine learning is making inferences on data from previous examples. ML can be considered a subfield of Artificial Intelligence.   

**Arthur Samuel (1959)**: Field of study that gives computers the ability to learn without being explicitly programmed. 

**Well-posed Learning Problem**   
**Tom Mitchell (1998)**: A computer program is said to learn from experience E, with respect to some task T, and some performance measure P, if its performance on T as measured by P improves with experience E. 

Example: Playing checkers  
  
E = the experience of playing many games of checkers

T = the task of playing checkers.

P = the probability that the program will win the next game.

**Supervised Learning** 
+ Most common.
+ Already know what our correct output should look like, having the idea that there is a relationship between the input and the output.
+ Supervised learning problems are categorized into "regression" and "classification" problems.

**Regresion:** Predict continuous valued output. Meaning that we are trying to map input variables to some continuous function. When the target variable that we’re trying to predict is continuous we call the learning problem a regression problem. 
Example: Given a picture of a person, we have to predict their age on the basis of the given picture

**Classification:** Discrete valued output. We are trying to map input variables into discrete categories. When y can take on only a small number of discrete values (such as if, given the living area, we wanted to predict if a dwelling is a house or an apartment, say), we call it a classification problem. 
Example: Given a patient with a tumor, we have to predict whether the tumor is malignant or benign (0 no / 1 yes) 

**Unsupervised Learning** 
+ Allows us to approach problems with little or no idea what our results should look like.
+ We can derive this structure by clustering the data based on relationships among the variables in the data.
+ With unsupervised learning there is no feedback based on the prediction results.

**Clustering:** Take a collection of 1,000,000 different genes, and find a way to automatically group these genes into groups that are somehow similar or related by different variables, such as lifespan, location, roles, and so on.

**Non-clustering:** The "Cocktail Party Algorithm", allows you to find structure in a chaotic environment. (i.e. identifying individual voices and music from a mesh of sounds at a cocktail party).

**m** = # of training examples / set  
**x**'s = "input" variable / features  
**y**'s = "outout" variable / "target" variable  


