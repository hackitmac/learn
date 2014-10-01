---
layout: workshop
module: rails
track: Web Developer
---
##Saving to DB & Showing our Articles

Now, we've created our model, and we have a table in our database called "Articles".  Let's go back and fix up the "create" function where we left off.

Replace it with the following

{% highlight css %}
def create
  @article = Article.new(params[:article])
 
  @article.save
  redirect_to @article
end
{% endhighlight %}

Here's what's going on: every Rails model can be initialized with its respective attributes, which are automatically mapped to the respective database columns. In the first line we do just that (remember that ```params[:article]``` contains the attributes we're interested in). Then, ```@article.save``` is responsible for saving the model in the database. Finally, we redirect the user to the show action, which we'll define later.

If you now go to [http://localhost:3000/articles/new](http://localhost:3000/articles/new) you'll almost be able to create an article. Try it! You should get an error that looks like ```ActiveModel::ForbiddenAttributesError in ArticlesController#create```

Rails has several security features that help you write secure applications, and you're running into one of them now. This one is called strong_parameters, which requires us to tell Rails exactly which parameters we want to accept in our controllers. In this case, we want to allow the title and body parameters, so add the new ```article_params``` method, and change your create controller action to use it, like this:

{% highlight css %}
def create
  @article = Article.new(article_params)
 
  @article.save
  redirect_to @article
end
 
private
  def article_params
    params.require(:article).permit(:title, :body)
  end
{% endhighlight %}

This lets Rails know that when we try to create an article, we require a variable for ```:article```, and we allow the variables ```:title``` and ```:body```.

If you submit the form again now, Rails will complain about not finding the show action. That's not very useful though, so let's add the show action before proceeding.

As we have seen in the output of ```rake routes```, the route for show action is as follows:
{% highlight css %}
article GET    /articles/:id(.:format)      articles#show
{% endhighlight %}

The special syntax ```:id``` tells rails that this route expects an ```:id``` parameter, which in our case will be the id of the article.

As we did before, we need to add the show action in ```/blog/app/controllers/articles_controller.rb``` and its respective view.

{% highlight css %}
def show
  @article = Article.find(params[:id])
end
{% endhighlight %}

A couple of things to note. We use Article.find to find the article we're interested in, passing in ```params[:id]``` to get the ```:id``` parameter from the request. We also use an instance variable (prefixed by @) to hold a reference to the article object. We do this because Rails will pass all instance variables to the view.

Now, create a new file ```/blog/app/views/articles/show.html.erb``` with the following content:

{% highlight css %}
<p>
  <strong>Title:</strong>
  <%= @article.title %>
</p>
 
<p>
  <strong>Text:</strong>
  <%= @article.body %>
</p>
{% endhighlight %}

With this change, you should finally be able to create new articles. Visit [http://localhost:3000/articles/new](http://localhost:3000/articles/new) and give it a try!

<p class="codelab-paging">
  <a href="../rails-6">Go to the next step &raquo;</a>
</p>