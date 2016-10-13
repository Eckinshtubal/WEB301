# Week #6

In week 6 we began looking into Bootstrap.

## Installation

First, go to the [Gulp Workflow Folder](../Resources/gulp-workflow/) and follow the instructions to get the Gulp Workflow up and running.

After this, the simplest way to install Bootstrap is to link to it from a CDN (Content Delivery Network). This involves making three changes to the `index.html` file (which can be found in the `app` folder).

1. Visit this link: http://getbootstrap.com/getting-started/#download-cdn
2. Copy the first link tag to the Bootstrap CSS and copy it into the HTML file - it **must** be placed above the existing CSS link.
3. Copy the **last** link (the second link is not required) to the Bootstrap JavaScript file, and paste it **above** the existing JavaScript link at the bottom of the HTML file.
4. One additional step is required, which is to add jQuery (Bootstrap requires jQuery to work).
5. Go to this link: http://getbootstrap.com/getting-started/#template
6. At the bottom of the provided code sample, copy the link to the jQuery file - this is around 5 lines up from the bottom.
7. Paste this into the HTML file **above** the Bootstrap JavaScript link at the bottom of the HTML file.

At this point, Bootstrap should be installed. You can confirm this by adding some Bootstrap styles to your HTML, for example:

```
<ul class="list-unstyled">
  <li>Item One</li>
  <li>Item Two</li>
</ul>
```
In this example, the `list-unstyled` class will remove the bull points from your unordered list.

Links to Materials & Resources

* [Installing Bootstrap the CDN way](https://www.youtube.com/watch?v=R52AsglN0DE)
* [Install Bootstrap from a CDN](http://htmlcheats.com/bootstrap/bootstrap-tutorial-cdn/)
* [Getting started with Bootstrap](http://www.w3schools.com/bootstrap/bootstrap_get_started.asp)
* [Bootstrap Cheat Sheet](https://www.cheatography.com/masonjo/cheat-sheets/bootstrap/)
