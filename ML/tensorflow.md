## What's TensorFlow?

TensorFlow was originally created by Google as an internal machine learning tool, but an implementation of it was open sourced under the Apache 2.0 License in November 2015.

*TensorFlow’s website:*

*Tagline:*
**"An open-source software library for Machine Intelligence"**

*Definition:*
TensorFlowTM is an open source software library for numerical computation using data flow graphs.

TensorFlow is one of more than a dozen of machine intelligence libraries developed by big companies and is probably one of the newest ones. For the list of current deep learning libraries, please visit this link.

*Tensors:* multilinear maps from vector spaces to the real numbers.

## Why TensorFlow?

Because it's created by Google. Duuuuuh. Really, among the listed deep learning libraries, the most popular libraries, are Theano, Torch, and TensorFlow. TensorFlow is new but it has already gained traction in both industries and research communities.

TensorFlow has a much cleaner interface as compared to Theano. Many classes of models can be expressed in significantly fewer lines without sacrificing the expressiveness of the framework. Furthermore, TensorFlow was built with production use in mind, whereas Theano was designed by researchers almost purely for research purposes. As a result, TensorFlow has many features out of the box and in the works that make it a better choice for real systems (the ability to run in mobile environments, to easily build models that span multiple GPUs on a single machine, and to train large-scale networks in a distributed fashion).

**TensorFlow pros:**

- Python API
- Portability: deploy computation to one or more CPUs or GPUs in a desktop, server, or mobile device with a single API
- Flexibility: from Raspberry Pi, Android, Windows, iOS, Linux to server farms
- Visualization (TensorBoard is da bomb)
- Checkpoints (for managing experiments)
- Auto-differentiation autodiff (no more taking derivatives by hand. Yasss)
- Large community (> 10,000 commits and > 3000 TF-related repos in one year)
- Awesome projects already using TensorFlow

**Companies using TensorFlow:**
- Google
- DeepMind
- OpenAI
- Snapchat
- Uber
- Airbus
- eBay
- Dropbox
- A bunch of startups

**Real world project using TensorFlow:**
- An enterprising Japanese cucumber farmer trained a model with TensorFlow to sort cucumbers by size, shape, and other characteristics.
- Radiologists have adapted TensorFlow to identify signs of Parkinson’s disease in medical scans.

TensorFlow provides an extensive suite of functions and classes that allow users to define models from scratch. This is more complicated but offers much more flexibility. You can build almost any architecture you can think of in TensorFlow.

**Virtualenv:**  
+ virtual Python environment isolated from other Python development, incapable of interfering with or being affected by other Python programs on the same machine.

```   
$ mkdir 'directory name'
$ cd 'directory name' 
$ virtualenv 'project name' 
```   

To use TensorFlow you have to activate the Virtualenv environment again if using bash.

```
$ source 'project name'/bin/ativate   
('project name')$  
# Your prompt should change. 
```

When done using TensorFlow, deactivate environment  

```
(tensorflow)$ deactivate  
# Your prompt should change back
```

List all packages installed   
```
$ pip list 
```

### Python 

Check python version  
```
$ python --version
```

Exit python in terminal  
```
$ exit()  
```

change python command 
```
$ alias python='python3'
```


