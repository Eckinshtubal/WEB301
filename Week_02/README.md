# Week #2 Resources

## Sass & media queries

## Sass

To compile a Sass file down to a CSS file:

1. Open terminal application from the dock.
2. Change directory to the folder where your sass file is located:

`cd /Users/web/desktop`

3. Alternatively type `cd ` and then drag the folder into the terminal window.
4. run the sass command:

`sass <input-file> <output-file>`

For example:

`sass main.scss output.css`

Note: the input file must always be a Sass file (ending in .scss) and the output file should be a CSS file.

## The watch command

It quickly becomes tedious to make changes to your Sass file and then follow the steps above to compile to a CSS file. The watch command allows Sass to run continuously, "watching" the Sass file for changes and compiling.

To run the command:

`sass --watch main.scss:output.css`

## Links to resources and materials

* [Sass home page](http://sass-lang.com/)
* [Sass basics](http://sass-lang.com/guide)
* [Installing Sass](http://sass-lang.com/install)
* [Sass primer for beginners](http://blog.teamtreehouse.com/the-absolute-beginners-guide-to-sass)
* [Sass cheat sheet](http://ricostacruz.com/cheatsheets/sass.html)

## Media queries

* [Media queries primer](http://unmatchedstyle.com/news/working-with-media-queries-and-min-width.php)
* [Tips and tricks with media queries](https://css-tricks.com/logic-in-media-queries/)
* [Overview of available media queries](http://cssmediaqueries.com/)
* [Some examples of sites built using media queries](http://mediaqueri.es/)
