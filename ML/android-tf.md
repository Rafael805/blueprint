Credit: The classifier example has been taken from Google TensorFlow example.

For this example we will be using a pre-trained model. 

# Building Process for Android

+ The core of the TensorFlow is written in c++.

+ In order to build for android, we have to use JNI(Java Native Interface) to call the c++ functions like loadModel, getPredictions, etc.

+ We will have a **.so**(shared object) file which is a c++ compiled file and a jar file which will consist of JAVA API that will be calling the native c++. And then, we will be calling the JAVA API to get things done easily.

+ We need the **jar**(Java API) and a **.so**(c++ compiled) file.

+ We must have the pre-trained model file and a label file for the classification.

**JNI**: Java Native Interface   

**jar**: Java API

**.so**: shared object 

**Android SDK**: Standard Development Kit

**Android NDK**: Native Development Kit 
