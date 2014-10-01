---
layout: workshop
module: rails
track: Web Developer
---

##Creating a Submission Form, and setting up Routes
Right now, we have a very barebones website, with nothing more than a static page.  Let's turn it into a simple blogging platform.  In the next sections, we will be creating an Article Model, a Controller to go with it, and Views that will give a user-friendly interface to interact with it all.

Remember that Rails likes us to split our websites in Models, Controllers, and Views.
First, we'll start by making a route so that we can get to our Controllers and Views when we make them.

Open up ```/blog/config/routes.rb``` in your text editor, and add the line
{% highlight css %}
resources :articles
{% endhighlight %}
This tells Rails that we want routes that link to a resource, called articles.  Resources are a standardised model in Rails, and they automatically generate four operations: Create, Read, Update, Destroy (CRUD)
What this means is that our articles can have routes leading to them: we can create articles, read articles, update articles, and destroy articles.

If you head back over to terminal and type 
{% highlight css %}
rake routes
{% endhighlight %}
You should see all the paths that are available.  We will be using the ```POST /articles(.:format) articles#create``` in the next section of this tutorial.

Now, we will work on the CRUD, let's start with Create.

If you head to [http://localhost:3000/articles/new](http://localhost:3000/articles/new) , you'll see a routing error ```uninitiaziled constant ArticlesController```
This error is telling us that we don't have a controller for our articles, so let's make one.  Head back over to your terminal:

{% highlight css %}
rails generate controller articles
{% endhighlight %}

This creates a controller called ```articles```, head back over to [http://localhost:3000/articles/new](http://localhost:3000/articles/new) and we're greeted with a new error, ```The action 'new' could not be found for ArticlesController```.  To fix this, let's head over to ArticlesController and create an action called new.

Open up ```/blog/app/controllers/articles_controller.rb```, and you should see an empty class.  Inside the class, create an empty action called new.
{% highlight css %}
def new
end
{% endhighlight %}

Again, open [http://localhost:3000/articles/new](http://localhost:3000/articles/new) , another error!  ```Template is missing```.  Rails is telling us that we have our Controller built, but that there is no View to link it to.


In Rails, the action ```new``` in ```/blog/app/controllers/articles_controller.rb``` corresponds with the template file ```/blog/app/view/articles/new.html.erb```.  Rails is complaining that this file doesn't exist.
We can fix this by heading over to ```/blog/app/view/articles/```, and creating a file called new.html.erb.

Fill it with the following:
{% highlight css %}
<h1>New Article</h1>
<%= form_for :article, url: articles_path do |f| %>
  <p>
    <%= f.label :title %><br>
    <%= f.text_field :title %>
  </p>
 
  <p>
    <%= f.label :body %><br>
    <%= f.text_area :body %>
  </p>
 
  <p>
    <%= f.submit %>
  </p>
<% end %>
{% endhighlight %}
####Code Explanation
{% highlight css %}
<h1>New Article</h1>
{% endhighlight %}
Shows the header, and the rest is the Rails form builder.
When you call form_for, you pass it an identifying object for this form. In this case, it's the symbol ```:article```. This tells the form_for helper what this form is for. Inside the block for this method, the FormBuilder object - represented by ```f``` - is used to build two labels and two text fields, one each for the title and body of an article. Finally, a call to submit on the f object will create a submit button for the form.

{% highlight css %}
<%= form_for :article, url: articles_path do |f| %>
{% endhighlight %}

```url: articles_path``` tells the form to look under "articles" in routes for a appropriate place to hook onto.  If you type rake routes, you will see this.  Forms, by default, hook onto POST events, of which there is only one.

If you head over back to [http://localhost:3000/articles/new](http://localhost:3000/articles/new), you should finally see a page with a submission form.

##Creating an Article
Try to create an article by clicking the create button.  You'll be greeted with yet another error:
```"Unknown action" The action 'create' could not be found for ArticlesController```.  Sounds familiar, right?  See if you can fix it yourself without reading the next line.

We will get around it by making another empty action in ```articles_controller.rb```:
{% highlight css %}
def create
end
{% endhighlight %}

Of course, this is a useless action, as it doesn't actually save anything to the database.

When a form is submitted, fields in the form are given to Rails as parameters.  These can then be accessed inside controllers.
Let's see what this looks like by printing out our variables.  We'll fill out the create method:
{% highlight css %}
def create
	render plain: params[:article].inspect
end
{% endhighlight %}

"render" tells rails to bypass looking for a view, because we're not going to keep this function, it's just for debugging purposes.
Go ahead and try to submit another article.

You should get something like this:
{% highlight css %}
{"title"=>"First article!", "body"=>"This is my first article."}
{% endhighlight %}

<p class="codelab-paging">
  <a href="../rails-4">Go to the next step &raquo;</a>
</p>