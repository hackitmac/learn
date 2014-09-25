---
layout: workshop
module: Intro to HTML & CSS
track: Web Developer
---

##Let's get set up
You should download the following:

+ Sublime Text([link](http://www.sublimetext.com/)) - a text editor with colour highlighting and other helpful features.
+ Google Chrome ([link](https://www.google.com/intl/en/chrome/browser/)) - Choose a modern web browser that supports current web standards and has good development tools. It's best to set a modern browser as your default browser.
+ Workshop files ([link](https://dl.dropboxusercontent.com/u/11788669/Project.zip)) - These are the files you will need for the workshop.

##Opening HTML files in your browser

###First, what is a browser?
The browser's main functionality is to present the web resource you choose, by requesting it from the server and displaying it in the browser window.
The web resource is usually an HTML document, but may also be a PDF, image, or other type.

###What is an HTML document?
Let's check out an example. Right-click and select View Page Source on this page. That's HTML.

![](http://i.imgur.com/OTlDWri.png)

We'll be learning to write our own HTML today. But first, let's open an HTML document (like the ones we'll create later) in our browser.

1. Open Sublime Text and go to File > Open.
2. Navigate to the Project folder (in the folder you downloaded with today's slides).
With the entire folder selected, click Open.
3. Now that the folder is open in Sublime, click on `blank.html` so that it fills the screen. Now, right click and select Open in Browser.

<div class="note tip">
  Don't be scared about breaking anything or doing something wrong. Play around, take risks, experiment and make mistakes. That's the best way to learn.

  <strong>And remember, ask a mentor (or Google) for help!</strong>
</div>

##What are HTML & CSS?
HTML & CSS are languages used to format how a website will look.

###HTML
**HTML** stands for **HyperText Markup Language**. But all you need to know is that it is a markup language. It tells the web browser what elements aka "content" to display. HTML uses a pre-defined set of [elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Element). HTML does not do the styling of the content.

Example HTML
{% highlight html %}
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>

</body>
</html>
{% endhighlight %}

###CSS

##Pratice
Try going through the interactive tutorials on [https://dash.generalassemb.ly/](https://dash.generalassemb.ly/.) to get more familar with html & css. When feel like you got the hang of html & css come back and finish this workshop.

##Looking up documentation or help
Get in the habit of looking things up and reading documentation.  
If you are looking up something about HTML/CSS use [https://developer.mozilla.org/en-US/](https://developer.mozilla.org/en-US/) instead of [http://www.w3schools.com/](http://www.w3schools.com/). W3schools can be outdated and has a lower quality of documentation. Reasons [http://www.w3fools.com/](http://www.w3fools.com/)

This can be done simply by adding `mdn` at the end of your searches.  
Ex. Search `div mdn` instead of `div`. First link will always be Mozilla Developer Network.

##Making our site
This is the site you willing be creating for this workshop ([preview](https://dl.dropboxusercontent.com/u/11788669/Project/final.html)).  
If you open up your `final.html` in your workshop folder. It will be this site. Feel free to reference it when you get stuck at the instructions.

![](http://i.imgur.com/hWtbJFW.png)

###Exercise: HTML markup for our final project
Let's write the HTML markup for our final project using what we just learned about headings, paragraphs and links.
Your page should look like this:

<p data-height="268" data-theme-id="8773" data-slug-hash="Cvajs" data-default-tab="result" data-user="jimicy" class='codepen'>See the Pen <a href='http://codepen.io/jimicy/pen/Cvajs/'>Cvajs</a> by jimmy wang (<a href='http://codepen.io/jimicy'>@jimicy</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
<script async src="//codepen.io/assets/embed/ei.js"></script>

Use `<h1></h1>` once, `<h2></h2>` three times and `<h3></h3>` once.  
You can also generate your own placeholder text at [http://www.lipsum.com](http://www.lipsum.com). Or, you can try Cupcake Ipsum, Bacon Ipsum or Samuel L. Ipsum for something fancy!

###Exercise: Add a logo & profile image to your project
The output (what you'll see in your browser) of this exercise is shown below. Write the HTML.

<p data-height="266" data-theme-id="8773" data-slug-hash="JeCfb" data-default-tab="result" data-user="jimicy" class='codepen'>See the Pen <a href='http://codepen.io/jimicy/pen/JeCfb/'>JeCfb</a> by jimmy wang (<a href='http://codepen.io/jimicy'>@jimicy</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
<script async src="//codepen.io/assets/embed/ei.js"></script>

Notice the images 

##Going live
Ok so you're comfortable with html & css and want to have your site on the **internet**. So how do you make it live?

###Hosting
To have a site live you will need someone to host your website. Since your site is consisted of static html files. Use Github pages. Github will host your site for free, [checkout this tutorial on hosting with Github](http://thephuse.com/development/hosting-static-sites-on-github-for-beginners/)

If you're wondering what's github [http://readwrite.com/2013/09/30/understanding-github-a-journey-for-beginners-part-1](http://readwrite.com/2013/09/30/understanding-github-a-journey-for-beginners-part-1)

###Domain Name
If you want a custom domain name something like `hackitmac.com` instead of `hackitmac.wordpress.com` or `hackitmac.github.io`. You will need to buy a domain name.

Namecheap is also offering free domain names for students to kickstart their online presence. Register with your mcmaster email. What are you waiting for, make that website you always wanted!  
[https://www.nc.me/](https://www.nc.me/)

![namecheap free domain](http://i.imgur.com/mbxdRbs.png)

If you're using github pages and you purchased a domain. [Here's how to get your site to redirect to your domain.](http://davidensinger.com/2013/03/setting-the-dns-for-github-pages-on-namecheap/)  
Basically have your site url be something like `hackitmac.com` instead of `hackitmac.github.io`.

##Next Steps
Check out our resources section. [hackitmac.com/learn/resources/](http://hackitmac.com/learn/resources/).

**Go on**  
[https://developer.mozilla.org/en-US/](https://developer.mozilla.org/en-US/). Explore around.

**Mozilla Developer Network has a great Web Developer guide section**  
[https://developer.mozilla.org/en-US/docs/Web/Guide](https://developer.mozilla.org/en-US/docs/Web/Guide)

**As well as a large tutorial list**  
[https://developer.mozilla.org/en-US/docs/Web/Tutorials](https://developer.mozilla.org/en-US/docs/Web/Tutorials)

Join our facebook group [fb.com/groups/hackitmac](http://fb.com/groups/hackitmac)

Come out to code nights. Every week tuesday 7pm-9pm IAHS Rm 103.  
Hang out, make new friends and continue learning to code with us :)!
