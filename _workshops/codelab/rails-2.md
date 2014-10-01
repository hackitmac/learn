---
layout: workshop
module: rails
track: Web Developer
---
##Making our first Controller and View
We don't need a model yet, because we're just trying to show a static page.
A ```controller``` is meant to recieve requests, which are directed to specific ```actions``` within it.  ```Actions``` are in charge of all the back-end logic, such as calculations needing to be done on a server, or accessing database entries, and providing that data to a View.
A ```view```, also known as a ```template```, is a layout (often written in css/html) in which the data is shown.


###Generating our controller
Head back to your terminal and type
{% highlight css %}
rails generate controller welcome index
{% endhighlight %}
This creates a controller called welcome, with an action index.  You can always add more actions later, but specifying it here lets rails generate the code for you, cutting out some work.

You'll see that files have been generated.  The files we are concerned with are the controller, ```/blog/app/controllers/welcome_controller.rb```, and the view, ```/blog/app/views/welcome/index.html.erb```.  Go ahead and open both of these in your text editor, we'll be working with them later.  For now, delete all the code in index.html.erb and type some text or code of your own.

###Routes
```Routes``` tell your application where to connect incoming requests to ```controllers``` and ```actions```.
Go ahead and open ```/blog/config/routes.rb```

Find the line containing ```root 'welcome#index'``` and uncomment it.
This tells rails that the root of your website should be directed to the controller ```welcome``` and the action ```index```, both of which you created in the last section.  Now go ahead and start up your server again, then browse to your page at [http://localhost:3000](http://localhost:3000)

Now, one of two things will happen...

+ Everything goes smoothly

+ or you get an ExecJS::Runtime Error

In the latter case, it is telling you that Rails needs a Javascript Runtime in order to work properly.  The easiest way to fix this is to install [NodeJS](http://nodejs.org), and try to restart your server and reload the page.  If it still gives you an error, you may need to restart your computer for NodeJS to take effect.

Once you have everything working, [http://localhost:3000](http://localhost:3000) should show the text that you typed into ```index.html.erb```.

<p class="codelab-paging">
  <a href="../rails-3">Go to the next step &raquo;</a>
</p>