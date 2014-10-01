---
layout: workshop
module: rails
track: Web Developer
---
##Updating (CRUD)
Not that we've finished the CR of our CRUD, let's move on to U.

The first step is to create an action ```edit``` in our ```articles_controller.rb```
{% highlight css %}
def edit
  @article = Article.find(params[:id])
end
{% endhighlight %}

The view will contain a form similar to the one we used when creating new articles. Create a file called ```app/views/articles/edit.html.erb``` and make it look as follows:

{% highlight css %}
<h1>Editing article</h1>
 
<%= form_for :article, url: article_path(@article), method: :patch do |f| %>
  <% if @article.errors.any? %>
  <div id="error_explanation">
    <h2><%= pluralize(@article.errors.count, "error") %> prohibited
      this article from being saved:</h2>
    <ul>
    <% @article.errors.full_messages.each do |msg| %>
      <li><%= msg %></li>
    <% end %>
    </ul>
  </div>
  <% end %>
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
 
<%= link_to 'Back', articles_path %>
{% endhighlight%}
This time we point the form to the update action, which is not defined yet but will be very soon.

The method: :patch option tells Rails that we want this form to be submitted via the PATCH HTTP method which is the HTTP method you're expected to use to update resources according to the REST protocol.

The first parameter of form_for can be an object, say, @article which would cause the helper to fill in the form with the fields of the object. Passing in a symbol (:article) with the same name as the instance variable (@article) also automagically leads to the same behavior. This is what is happening here.

Next we need to create the update action in ```/blog/app/controllers/articles_controller.rb:```
{% highlight css %}
def update
  @article = Article.find(params[:id])
 
  if @article.update(article_params)
    redirect_to @article
  else
    render 'edit'
  end
end
 
private
  def article_params
    params.require(:article).permit(:title, :body)
  end
{% endhighlight%}

Finally, we want to show a link to the edit action in the list of all the articles, so let's add that now to app/views/articles/index.html.erb to make it appear next to the "Show" link:

{% highlight css %}
<table>
  <tr>
    <th>Title</th>
    <th>Text</th>
    <th colspan="2"></th>
  </tr>
 
<% @articles.each do |article| %>
  <tr>
    <td><%= article.title %></td>
    <td><%= article.body %></td>
    <td><%= link_to 'Show', article_path(article) %></td>
    <td><%= link_to 'Edit', edit_article_path(article) %></td>
  </tr>
<% end %>
</table>
{% endhighlight%}

###Deleting
We're almost done our CRUD!  Let's work on the final part, Deleting.

Define the delete action in our Articles Controller:
{% highlight css %}
def destroy
  @article = Article.find(params[:id])
  @article.destroy
 
  redirect_to articles_path
end
{% endhighlight%}

And add a delete link next to ```Show``` and ```Update```
{% highlight css %}
<td><%= link_to 'Destroy', article_path(article),
                    method: :delete, data: { confirm: 'Are you sure?' } %></td>
{% endhighlight%}


##Yay, we're done!
If you find it interesting, you can try to add user logins using the [devise gem](https://github.com/plataformatec/devise)

This was a stripped down, simplified version of the [Official Rails Getting Started Tutorial](http://guides.rubyonrails.org/getting_started.html)