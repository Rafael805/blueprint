# What is a Virtualenv

What virtualenv does is pretty simple, but highly useful: it copies your system Python install along with supporting packages to a directory associated with your project, and then updates the Python paths to point to this copied environment. That way you can pip install to your heart’s content, without making any changes to your global Python install. 

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
