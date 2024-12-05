# About Images & Other Files

[Back to overview](../README.md)

If you want to include an image (or video or audio file) in your
webpage, you will need to upload it as a "static" file to your site.
Unlike the `.astro` files, images don't need to be processed by
code before being added to your website: they will end up being
referenced and downloaded directly.

## Where to Upload

You should upload images and other static files into the `/public/`
folder. If you think you'll have a lot of files, you can create
folders inside of `/public/` like `/images/`.

## How to reference the URL

When your site is built, the images will be at the "base URL" of your
site, so if you are at "index.astro" you can reference them directly
as `"cat.jpg"` or `"images/cat.jpg"` if you put them in a folder
called images. If you are the projects folder, you will need to use
the `../` reference to move back a folder, like `"../../images/cat.jpg"`

## How to insert an Image in your Project

There are usually _two_ ways that web pages use images: either as
content itself or as a background.

### As Content

As content, you just need to create an image tag, which is `img`, like
this:

```html
<img src="images/cat.jpg" alt="a cute cat" />
```

### As a background

If you want the image to be a background, you can either use your
`styles.css` file or you can insert a `style=` attribute in your
HTML. Here's what that looks like:

#### With the stylesheet

```css
body {
  background-image: url("images/cat.jpg");
  background-size: cover;
  background-position: center;
}
```

#### With the style attribute

The style attribute could be added to _any_ HTML tag

```html
<section
  style="background-image: url('cat');background-size:cover;background-position: cover;"
>
  ...
</section>
```
