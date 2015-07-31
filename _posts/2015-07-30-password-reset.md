---
layout: post
title: Password Reset in Nodejs
description: "In this tutorial, we will create a login module along with a signup and password functionality in Nodejs using Sequelizer with Postgresql"
headline: "Password Reset in Nodejs"
categories: Nodejs Express Sequelize Nodemailer Postgresql
tags: 
  - Nodejs
imagefeature: "password-reset3.jpg"
imagecredit: http://cryptobizmagazine.com/
imagecreditlink: "http://cryptobizmagazine.com/wp-content/uploads/2014/06/shutterstock_122234134-medium.jpg"
comments: false
mathjax: null
featured: true
published: true
---

In this tutorial, we will create a login module along with a signup and password functionality in Nodejs using Sequelizer with Postgresql and Nodemailer.

{% highlight bash %}
sudo npm install -g express-generator
{% endhighlight %}



{% highlight javascript %}
var express = require('express');
var path = require('path');
var favicon = require('static-favicon');
var logger = require('morgan');
var cookieParser = require('cookie-parser');
var bodyParser = require('body-parser');

var app = express();

// Middleware
app.set('port', process.env.PORT || 3000);
app.set('views', path.join(__dirname, 'views'));
app.set('view engine', 'jade');
app.use(favicon());
app.use(logger('dev'));
app.use(bodyParser.json());
app.use(bodyParser.urlencoded());
app.use(cookieParser());
app.use(express.static(path.join(__dirname, 'public')));

// Routes
app.get('/', function(req, res) {
  res.render('index', { title: 'Express' });
});

app.listen(app.get('port'), function() {
  console.log('Express server listening on port ' + app.get('port'));
});
{%  endhighlight %}

{% highlight css %}
#container {
  float: left;
  margin: 0 -240px 0 0;
  width: 100%;
}
{% endhighlight %}

<pre>
  <code class="ruby">
    puts "hello"
  </code>
</pre>


