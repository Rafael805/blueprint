## What Is A Jupyter Notebook?

Jupyter Notebook App (formerly IPython Notebook) is a web-based application suitable for capturing the whole computation process: developing, documenting, executing code, and communicating the results. You can create and share documents that contain live code, equations, visualizations as well as text. Notebook don't require users to refresh the whole page every time you do something.

web application: a client–server software application in which the client (or user interface) runs in a web browser.

The application can be executed on a PC without Internet access or it can be installed on a remote server, where you can access it through the Internet. Its two main components are the kernels and a dashboard.

kernel: a program that runs and introspects the user’s code.

The Jupyter Notebook App has a kernel for Python code, but there are also kernels available for other programming languages.

## What Is The Jupyter Notebook App?

The main components of the whole environment are the notebooks themselves and the application. On the other hand, you also have a notebook kernel and a notebook dashboard.

Notebook documents (or “notebooks”) are documents produced by the Jupyter Notebook App, which contain both computer code (e.g. python) and rich text elements (paragraph, equations, figures, links, etc...). Notebook documents are both human-readable documents containing the analysis description and the results (figures, tables, etc..) as well as executable documents which can be run to perform data analysis.

Notebook documents: a representation of all content visible in the web application, including inputs and outputs of the computations, explanatory text, mathematics, images, and rich media representations of objects.

Note: "Jupyter" is a loose acronym meaning Julia, Python, and R. These programming languages were the first target languages of the Jupyter application, but nowadays, the notebook technology also supports many other languages.

## Main Features
+ In-browser editing for code, with automatic syntax highlighting, indentation, and tab completion/introspection.
+ The ability to execute code from the browser, with the results of computations attached to the code which generated them.
+ Displaying the result of computation using rich media representations.
+ In-browser editing for rich text using the Markdown markup language, which can provide commentary for the code, is not limited to plain text.
+ The ability to easily include mathematical notation within markdown cells.

## Getting Started With Jupyter Notebooks
You can start running a notebook server from the command line using the following command:
```
jupyter notebook
```  
Then you'll see the application opening in the web browser on the following address: http://localhost:8888.  

The "Files" tab is where all your files are kept, the "Running" tab keeps track of all your processes and the third tab, "Clusters", is provided by IPython parallel, IPython's parallel computing framework. It allows you to control many individual engines, which are an extended version of the IPython kernel.

## Creating a new notebook document

A new notebook may be created at any time, either from the dashboard, or using the File ‣ New menu option from within an active notebook. The new notebook is created within the same directory and will open in a new browser tab. It will also be reflected as a new entry in the notebook list on the dashboard.
