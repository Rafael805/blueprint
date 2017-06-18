# What's TensorFlow?

TensorFlow was originally created by Google as an internal machine learning tool, but an implementation of it was open sourced under the Apache 2.0 License in November 2015.

*TensorFlow’s website:*

*Tagline:*
**"An open-source software library for Machine Intelligence"**

*Definition:*
TensorFlowTM is an open source software library for numerical computation using data flow graphs.

TensorFlow is one of more than a dozen of machine intelligence libraries developed by big companies and is probably one of the newest ones. For the list of current deep learning libraries, please visit this link.

### Tensors
Multilinear maps from vector spaces to the real numbers. The central unit of data in TensorFlow is the **tensor**. A tensor consists of a set of primitive values shaped into an array of any number of dimensions. 

### Tensor's rank

# Why TensorFlow?

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

# Inception
+ One of Google's best image classifiers 
+ Open source 
+ Trained 1.2 million images 

# TF Learn 
+ High level ML library on top of TensorFlow
+ Similar to scikit-learn

## Importing Tenstorflow 

To give Python access to all of TensorFlow's classes, methods, and symbols:
```
import tensorflow as tf
```
# Computational graph
Computational graph is a series of TensorFlow operations arranged into a graph of nodes. Each node takes zero or more tensors as inputs and produces a tensor as an output. One type of node is a constant. Like all TensorFlow constants, it takes no inputs, and it outputs a value it stores internally.

```
node1 = tf.constant(3.0, tf.float32)
node2 = tf.constant(4.0) # also tf.float32 implicitly
print(node1, node2)
```

Output:
```Tensor("Const:0", shape=(), dtype=float32) Tensor("Const_1:0", shape=(), dtype=float32)```

printing the nodes does not output the values ```3.0``` and ```4.0``` because they are nodes that, when evaluated, would produce ```3.0``` and ```4.0```. To actually evaluate the nodes, you must run the computational graph within a **session**. A session encapsulates the control and state of the TensorFlow runtime.

Creates a ```Session``` object and then invoke its ```run``` method to run enough of the computational graph to evaluate ```node1``` and ```node2```.

```
sess = tf.Session()
print(sess.run([node1, node2]))
```

Expected output:
```[3.0, 4.0]```

We can build more complicated computations by combining **Tensor nodes** with operations (Operations are also nodes). For example, we can add our two constant nodes and produce a new graph as follows:

```node3 = tf.add(node1, node2)
print("node3: ", node3)
print("sess.run(node3): ",sess.run(node3))
```

Expected output: 
```
node3:  Tensor("Add_2:0", shape=(), dtype=float32)
sess.run(node3):  7.0
```

### TensorBoard
TensorFlow provides a utility called TensorBoard that can display a picture of the computational graph.

### Placeholders
A graph can be parameterized to accept external inputs, known as **placeholders**. A placeholder is a promise to provide a value later.

```
a = tf.placeholder(tf.float32)
b = tf.placeholder(tf.float32)
adder_node = a + b  # + provides a shortcut for tf.add(a, b)
print(sess.run(adder_node, {a: 3, b:4.5}))
print(sess.run(adder_node, {a: [1,3], b: [2, 4]}))
```

Expected output: 
```
7.5
[ 3.  7.]
```





