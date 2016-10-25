# Week 8

Your client has supplied you with a mockup showing mobile, tablet and desktop layouts.

They have also provided you with the images for the carousel. It has been decided to use Bootstrap for this project.

We will be looking at some techniques and tricks along the way, but how close can you get to the mockups?

## A Little Trick: An Image Placed Within a DIV Centered Vertically

Given this code:

```
<div class="full-width-image">
  <img src="/my/img/file.png">
</div>
```
This CSS will center the image vertically within the DIV:

```
.full-width-image {
   border: 1px solid red;
    overflow: hidden;
    position: relative;
    height: 200px;
    @media (min-width: 768px) {
        height: 350px;
    }
}

.carousel-images {
    width: 100%;
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
}
```
