
_______________________________________________

# CodeSchool Notes

## codeschool - node.js - 5.1 Express
- Express is a framework for node 
- "Sinatra inspired web development framework for Node.js - insanely fast, flexible and simple"
- Easy route URLs to callbacks 
- Middleware (from Connect)
- Environment based configuration 
- Redirection helpers
- File Uploads 

```javascript
npm install --save express // install the module and adds to package.json 
var express = require('express'); 
var app = express(); // to create an instance of express 

app.get('/', function(request, response) {
  response.sendFile(__dirname + '/index.html')
  }
})
app.listen(8080); 
```

```javascript
var request = require('request');
var url = require('url'); 

app.get('/tweets/:username', function(req, response) {
  var username = req.params.username; 

  options = {
    protocol: "http:"
    host: 'api.twitter.com',
    pathname: '/1/statuses/user_timeline.json', 
    query: { screen_name: username, count: 10}
  }

  var twitterUrl = url.format(options); 
  request(twitterUrl).pipe(response); //pipe the request to response 
  })
```






_______________________________________________


## codeschool - node.js - 5.2 
















