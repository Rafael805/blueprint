# Initialize Express 

```
var express = require("express");  
var app = express(); 
```

# Simple Routes 

Route definition takes the following structure:

```
app.METHOD(PATH, HANDLER)
```

Where:

``app``: instance of express.  
``METHOD``:  HTTP request method, in lowercase.  
``PATH``: path on the server.  
``HANDLER``: function executed when the route is matched.  

Respond with Hello World! on the homepage:

```
app.get('/', function (req, res) {
  res.send('Hello World!')
})
```

Respond to POST request on the root route (/), the application’s home page:

```
app.post('/', function (req, res) {
  res.send('Got a POST request')
})
```

Respond to a PUT request to the /user route:

```
app.put('/user', function (req, res) {
  res.send('Got a PUT request at /user')
})
```

Respond to a DELETE request to the /user route:

```
app.delete('/user', function (req, res) {
  res.send('Got a DELETE request at /user')
})
```

# Serving static files in Express
To serve static files such as images, CSS files, and JavaScript files, use the ```express.static``` built-in middleware function in Express.

Pass the name of the directory that contains the static assets to the ```express.static``` middleware function to start serving the files directly. This specifies a folder name that we want to expose to the web server. For example, use the following code to serve images, CSS files, and JavaScript files in a directory named ```public```:
```
app.use(express.static('public'));
```

Now, you can load the files that are in the public directory.

# Start server
Takes two functions. The port which is 3000 and the function that will be called once the server is up. The app starts a server and listens on port 3000 for connections. 
```
app.listen(3000, function () {
  console.log('Example app listening on port 3000!')
})
```
Then, load http://localhost:3000/ in a browser to see the output.

--example: 
```
var express = require('express');
var app = express();

app.get("/", function (req, res) {
  res.send("Hello World, from our web app!");
});

app.listen(8080, function() {
  console.log('App listening on port 8080!');
});
```
