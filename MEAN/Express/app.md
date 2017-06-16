Route definition takes the following structure:

```
app.METHOD(PATH, HANDLER)
```

Where:

``app``: instance of express.  
``METHOD``:  HTTP request method, in lowercase.  
``PATH``: path on the server.  
``HANDLER``: function executed when the route is matched.  

## Initialize Express 

```
var express = require("express");  
var app = express; 
```

## Simple Routes 

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
Respond to a DELETE request to the /user route:

app.delete('/user', function (req, res) {
  res.send('Got a DELETE request at /user')
})
