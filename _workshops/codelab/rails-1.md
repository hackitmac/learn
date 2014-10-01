---
layout: workshop
module: rails
track: Web Developer
---

##Let's get set up

You'll want to install Sublime Text, or open up your favourite editor, along with Ruby on Rails for your OS.

###[Sublime Text](http://www.sublimetext.com/)

###[Ruby on Rails (Windows)](https://github.com/railsinstaller/railsinstaller-windows/releases/download/3.0.0-alpha.2/railsinstaller-3.0.0.exe)

###[Ruby on Rails (Linux)](http://rvm.io/rvm/install)


##Getting Started
Open up your command prompt or terminal, and cd into your working directory.
We're going to be making a basic blogging application, so let's create a new project called "blog".  In your terminal, type
{% highlight css %}
rails new blog 
{% endhighlight %}

When this command finishes running, you should see that a bunch of files have been generated, go ahead and look around.
99% of the stuff that you regularly need will be in one of three folders: ```/blog```, ```/blog/config```, and ```/blog/app```.

Once you're done looking around, go back to your terminal and type
{% highlight css %}
rails server
{% endhighlight %}

This will start a Rails development server on your machine, that you can access by browsing to [http://localhost:3000](http://localhost:3000)

You should see a default Rails page.  Press Ctrl+C on your Terminal to stop the server.



<p class="codelab-paging">
  <a href="../rails-2">Go to the next step &raquo;</a>
</p>