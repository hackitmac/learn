---
layout: workshop
module: rails
track: Web Developer
---
##Listing Articles
Most blogs have a way to list all the articles, so we're going to do that next.
Remember that rake routes gives us the following for "index"

{% highlight css %}
articles GET    /articles(.:format)          articles#index
{% endhighlight %}

Add the corresponding index action for that route inside the ArticlesController in the ```/blog/app/controllers/articles_controller.rb``` file:
{% highlight css %}
def index
  @articles = Article.all
end
{% endhighlight%}
And then finally, add view for this action, located at ```/blog/app/views/articles/index.html.erb```:
{% highlight css %}
<h1>Listing articles</h1>
 
<table>
  <tr>
    <th>Title</th>
    <th>Text</th>
  </tr>
 
  <% @articles.each do |article| %>
    <tr>
      <td><%= article.title %></td>
      <td><%= article.body %></td>
    </tr>
  <% end %>
</table>
{% endhighlight%}

##Adding Links
Right now, we have our blog basically working, but there's no links, and we have to type the urls to get to our pages.


Open up ```/blog/app/views/articles/index.html.erb```, and add the following code to the bottom:
{% highlight css %}
<%= link_to 'New article', new_article_path %>
{% endhighlight%}
####Code Explanation
In .erb files, ```<%=``` and ```%>``` are the tags that tell Rails to run Ruby code, rather than just printing out as html.
We call ```link_to``` with two arguments, the first one, ```'New article'```, is the text that will be displayed, and ```new_article_path``` is where the link leads to.

Next, we'll add "back" links to our articles, and our article creation forms by putting
{% highlight css %}
<%= link_to 'Back', articles_path %>
{% endhighlight%}
in ```/blog/app/views/articles/new.html.erb``` and ```/blog/app/views/articles/show.html.erb```

We also want to add links from the list of articles, to each individual article, so add the line
{% highlight css %}
<td><%= link_to 'Show', article_path(article) %></td>
{% endhighlight %}
into your ```/blog/app/views/articles/index.html.erb``` below the body for each article.

<p class="codelab-paging">
  <a href="../rails-7">Go to the next step &raquo;</a>
</p>