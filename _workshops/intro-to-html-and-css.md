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

(If your default browser isn't set to Chrome, [here are the instructions](https://support.google.com/chrome/answer/95417?hl=en).)

####You should see something like this:
![](http://i.imgur.com/CsIvpo3.png)

###Now, let's make a change to our file and re-open it in our browser.
1. Try changing something, like the text within the `<p></p>` tags.
2. Save your file using **File > Save**, or use keyboard shortcuts (<span class="keyboard">CMD</span>+<span class="keyboard">S</span> or
<span class="keyboard">CONTROL</span>+<span class="keyboard">S</span>)
3. Right click and select Open in Browser.
4. Change something else and open it in your browser again, just to make sure you've got it!
5. After saving, you can also just refresh your browser to see the changes (rather than opening your file in a new tab every time).

<div class="note tip">
  Don't be scared about breaking anything or doing something wrong. Play around, take risks, experiment and make mistakes. That's the best way to learn.

  <strong>And remember, ask a mentor (or Google) for help!</strong>
</div>

##What are HTML & CSS?
HTML & CSS are languages used to format how a website will look.

###HTML (HyperText Markup Language)
HTML is used to describe each part of a webpage to the browser. It tells the web browser what elements to display. HTML uses a pre-defined set of [elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Element).

To display content properly in the browser, we use tags to start and end an element. Here are a few examples of common HTML tags:

This starts and ends a `h1` header1 element.

+ `<h1>` and `</h1>`.

This starts and ends a `p` paragraph element.

+ `<p>` and `</p>`.

This starts and ends a `strong` which is a bolded + emphasized element

+ `<strong>` and `</strong>`.

For the browser to recogize these tags as HTML, we need to create an HTML file.

####Good file naming habits
To create an HTML web page, just name your file using the .html extension (much like .pdf for PDF files or .doc for Word files).

+ Use lowercase letters.
    * `about.html` instead of `About.html` or `ABOUT.html`
+ Avoid s p a c e s. Use underscores (_) or dashes (-). Dashes are generally preferred for SEO (search engine optimization).
    * `business_hours.html` or `business-hours.html` instead of `business hours.html`
(The browser will interpret it as `business%20hours.html`)
+ Avoid symbols like `# & *` in your file name.
+ Keep your file names concise, yet meaningful.
    * about.html, contact.html instead of page1.html, page2.html

These file naming tips can be applied to any type of files such as images, folders, CSS, etc.

####Quick exercise: Saving a new file as an HTML file
1. In Sublime Text, click **File > New File**
2. By default, the file type is plain text, not HTML. You have two choices for saving this file as an HTML file.
    * Option 1: On the bottom right corner, you should see the words Plain Text. Click it and select HTML from the list. Save the file using (<span class="keyboard">CMD</span>+<span class="keyboard">S</span> or
<span class="keyboard">CONTROL</span>+<span class="keyboard">S</span>). Name it anything but be sure it ends with `.html`. You can save the file anywhere - we won't be using it for anything else.
    * Option 2: From the menu bar, select **File > Save As**. Give your file a name and add `.html` at the end. Click save.

####Nut & Bolts of HTML
When writing HTML, we create HTML elements by wrapping our content in tags. These tags describe the content that is inside of them, NOT what they look like.

For example, the paragraph tag (`<p>paragraph content</p>`) is used to describe the content in between as being a paragraph, not it's color or any other style.

We use different kinds of tags to create multiple elements and all together they make up our HTML Document.

It is important to understand that HTML has very little to do with the style of your website or the look of the content - that is what CSS is for.

####Tags that you should no longer use!
It’s very important to create semantic, clean and valid markup before doing anything else. Older versions of HTML used to include tags that were used for defining styles, which is now handled with CSS instead.

Here are a few examples of old tags that are **no longer used:**

+ `<u>`I'm underlined!`</u>`
+ `<marquee>`Anyone remember the marquee tag?`</marquee>`
+ `<font size="large">`HUGE FONTS!`</font>`
+ `<center>`I'm centered text!`</center>`
+ `<b>`I'm Bold text!`</b>`*
+ `<i>`I'm Italic!`</i>`*

###CSS (Cascading Style Sheets)
CSS is the presentation layer. In other words, it makes websites look nice.  
HTML tells the browser what different parts of the page mean, CSS tells the browser what those parts should look like.  
For example, p means paragraph in HTML. But if we wanted to make all of our paragraphs red and underlined, in CSS we'd do something like this:

{% highlight css %}
p {
  color: red;
  text-decoration: underline;
}
{% endhighlight %}

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

Notice the images have `src="http://i.imgur.com/f6zv8kZ.png"` this means the image is hosted online. But you'll probably want to do something like `src="images/profile.jpg"`

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
