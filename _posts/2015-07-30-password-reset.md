---
layout: post
title: Password Reset in Nodejs
description: "In this tutorial, we will create a login module along with a signup and password functionality in Nodejs using Sequelizer with Postgresql"
headline: "Password Reset in Nodejs"
categories: Blog
tags: 
  - Nodejs
  - Express
  - Sequelize
  - Postgresql
  - Nodemailer
imagefeature: "password-reset3.jpg"
imagecredit: http://cryptobizmagazine.com/
imagecreditlink: "http://cryptobizmagazine.com/wp-content/uploads/2014/06/shutterstock_122234134-medium.jpg"
comments: false
mathjax: null
featured: true
published: true
---

In this tutorial, we will create a complete login module containing a forgot your password feature and sign up form using Express, Sequelize with Postgresql, and Nodemailer.                             

To start off, we will begin with some express basics. Let's first install express-generator globally which will create an express project skeleton for us. For our convenience, we will also install nodemon which will watch for any file changes in which it was started and if any file changes, it will restart the nodejs application automatically for us with the latest changes. Execute the following command in your command line: 

{% highlight bash %}
npm install -g express-generator nodemon
{% endhighlight %}

To create a new express project, run: 

{% highlight bash %}
express PasswordReset
{% endhighlight %}

This will create a new folder called PasswordReset with the following structure: 

{% highlight bash %}
.
├── app.js
├── bin
│   └── www
├── package.json
├── public
│   ├── images
│   ├── javascripts
│   └── stylesheets
│       └── style.css
├── routes
│   ├── index.js
│   └── users.js
└── views
    ├── error.jade
    ├── index.jade
    └── layout.jade
{% endhighlight %}

Afterwards, we need to install all express dependencies locally by first changing our current directory to our project and running: 

{% highlight bash %}
npm install
{%  endhighlight %}

To keep the app architecture simpler, let's delete the bin folder and delete the users.js file inside the routes directory since we will not be using it. 

Now we will need to make some minor adjustments to app.js. First, locate the following line and delete it.
{% highlight javascript  %}
app.use('/users', users);
{% endhighlight %}

Then we will set the port we want to run our application to run on by passing an extra argument during startup or run it by default on port 3000.

{% highlight javascript  %}
// filename: app.js
app.set('port', process.argv[2] || 3000);
app.listen(app.get('port'), function() {
  console.log('Express server listening on port ' + app.get('port'));
});
{% endhighlight %}

Before running the application, we need to update the package.json 'start' command to use nodemon and run our app.js instead of the now deleted bin/www.

{% highlight javascript %}
// package.json
"scripts": {
    "start": "nodemon app.js"
}
{% endhighlight %}

Alas, we can run our application with {% highlight bash  %}npm start {% endhighlight %} and feast our eyes upon the "Welcome to Express" page. 

<div class="row" style="border-width:1px; border-style:solid;border-color:black">
    <img src='{{ site.url }}/images/password-reset/welcome-to-express-page.png' />
</div>



