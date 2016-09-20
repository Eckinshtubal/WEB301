# Week #3

## The viewport meta tag

It's important to remember when using media queries, you must add a `<meta>` tag to the head of your HTML document.

For basic usage the tag can simply be:

```
<meta name="viewport" content="width=device-width">
```

However, you can also set an initial size:

```
<meta name="viewport" content="width=device-width, initial-scale=1">
```

And you might want to specify whether or not the user can zoom in or not:

```
<meta name="viewport" content="initial-scale=1.0, user-scalable=no" />
```

## Media Queries

The most basic media query specifies a minimum or maximum size:

```
@media (min-width: 768px) {
  /* styles here */
}
```
However, media queries can also be combined for more specific targeting:

```
@media (min-width: 768px) and (max-width: 992px) {
  /* styles here */
}
```

## Types of media queries

Media queries can also target devices and media by other means. For example, you can specify media queries by `all`, `print` and `screen` like so:

```
@media all {
  body {
    width: 100;
  }
}

@media screen {
  body {
    width: 75%;
  }
}

@media print {
  body {
    width: 50%;
  }
}
```

**IMPORTANT:** Stacking and combining media queries can become cumbersome quickly! Think about what you need to achieve and plan things out a little first.

The most complex media query I could find online:

```
@media
  only screen and (min-width: 100px),
  not all and (min-width: 100px),
  not print and (min-height: 100px),
  (color),
  (min-height: 100px) and (max-height: 1000px),
  handheld and (orientation: landscape)
{
  html { background: red; }
}
```

Can you figure out what this media query is targeting?

---

# Sass extend

The Sass `@extend` feature allows you to create multiple classes from a single class. For example:

```
.btn {
  display: inline-block;
  text-decoration: none;
  border-radius: 3px;
  color: #fff;
}

.red-btn {
  @extend .btn;
  background-color: red;
}

.green-btn {
  @extend .btn;
  background-color: green;
}
```

# Sass mixins

Sass `@mixin` works similarly to `@extend`, except it allows you to add additional variables:

```
@mixin border-radius($radius) {
  border-radius: $radius;
}

.btn1 {
  @include border-radius(3px);
}

.btn2 {
  @include border-radius(6px);
}

.btn3 {
  @include border-radius(9px);
}
```

You can create more complex mixins, here's a set I use frequently in my projects:

```
@mixin mobile-up {
  @media (min-width: 320px) { @content; }
}
@mixin tablet-up {
  @media (min-width: 768px) { @content; }
}
@mixin desktop-up {
  @media (min-width: 992px) { @content; }
}
@mixin widescreen-up {
  @media (min-width: 1200px) { @content; }
}
```
This allows for simple media query "shortcuts" like this:

```
.btn {
  display: block;
  @include mobile-up {
    display: inline-block;
  }
}
```

---

# Links to resources and materials

* [The responsive meta tag](https://css-tricks.com/snippets/html/responsive-meta-tag/)
* [Media queries cheat sheet](http://mac-blog.org.ua/css-3-media-queries-cheat-sheet/)
* [Logic in media queries](https://css-tricks.com/logic-in-media-queries/)
* [A gallery of sites using media queries](http://mediaqueri.es/)
* [An image showing the number of possible screen sizes](https://gigaom2.files.wordpress.com/2014/01/android-screen-sizes.jpg)
* [Sass Guide covering inheritance/extend and mixins](http://sass-lang.com/guide)
* [Sass extend](https://css-tricks.com/the-extend-concept/)
* [Example: using Sass to create CSS triangles](https://www.sitepoint.com/sass-mixin-css-triangles/)
