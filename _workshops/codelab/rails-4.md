---
layout: workshop
module: rails
track: Web Developer
---
##Models
We're still missing our model, so all of this data can get sent to our Rails application, but it has nowhere to go from there.  Let's create the Article model so that we can save to the database.

Models in Rails use a singular name, and their corresponding database tables use a plural name.  Rails automatically generates the database, so you just have to make a model and define it's properties.

{% highlight css %}
rails generate model Article title:string body:text
{% endhighlight %}

What this does is tell Rails to create a model migration, of a model called Article, which has the "Title" of type "string", and "body" of type "text"

If you look in the ```/blog/db/migrate/2014XXXXXXXX_create_articles.rb``` file, you will see the actions that rails will take once you tell it to migrate the change.

Head back over to your terminal:
{% highlight css %}
rake db:migrate
{% endhighlight %}

Rails should spit out a few lines telling you that it was a successful migration.

<p class="codelab-paging">
  <a href="../rails-5">Go to the next step &raquo;</a>
</p>