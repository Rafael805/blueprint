Route definition takes the following structure:

```
app.METHOD(PATH, HANDLER)
```

Where:

``app``: instance of express.
``METHOD``:  HTTP request method, in lowercase.
``PATH``: path on the server.
``HANDLER``: function executed when the route is matched.


var express = require("express");
var app = express;

