# My Boilerplate #

*Created and authored by [Michael Manhire](http://www.michaelmanhire.com/)*
*Although it was developed for my own purposes, anyone may use this boilerplate if they so choose*

## HTML ##

### HTML5 Doctype ###

Unless you are using an older version of HTML, always include `<!DOCTYPE html>`.

### Language Attribute ###

You should specify the language of your content by adding the `lang` attribute to `<html>`.

### Essential Meta Tags ###

The first meta tag should indicate the character set that is used. Generally, you should use `<meta charset="utf-8">` as it contains a lot of characters and simplifies character handling in documents using different scripts.

Include `<meta http-equiv="x-ua-compatible" content="ie=edge">` next. Internet Explorer 8/9/10 support document compatibility modes that affect the way webpages are interpreted and displayed. Including this meta tag will ensure that older versions of Internet Explorer render the webpage in the highest available mode.

Place `<meta name="viewport" content="width=device-width, initial-scale=1">` next to ensure that your website is responsive on mobile devices.

### Title ###

Add the name of your website to the `<title>` element.

### Other Meta Tags ###

Set the author of the document with the `name="author"` attribute.

Set a description that will be indexed by search engines with the `name="description"` attribute. Note that search engines generally truncate descriptions that are longer than 160 characters.

Direct robots' behavior with the `name="robots"` attribute. Common values (separated by commas) for this are:
* `index` and `noindex` tell the robot whether or not it should allow people to find this webpage through search engines.
* `follow` and `nofollow` tell the robot whether or not it should follow links on this page to other webpages.

The [Open Graph](http://ogp.me/) meta tags specify how pages should look when they are linked to on websites like Facebook and Google Plus. Rather than using the `name` attribute, they use the `property` attribute. If you decide to specify Open Graph meta information, you must provide the following property values:
* `og:title` is the title of your webpage, often the same as the `<title>` element.
* `og:type` is `website`; however, there may be more appropriate values like `article` or `profile` and these may require other properties. If you are unsure, seek outside resources.
* `og:image` is an image URL that represents your webpage. This may be the favicon, although it should be much larger resolution.
* `og:url` is the canonical URL of your webpage.

The following property values are optional:
* `og:description` is a one to two sentence description of the webpage, often the same as the `<meta name="description">` element.
* `og:site_name` should be used if your webpage is part of a larger website, the name (not the URL) of which should be expressed in this property.

The [Twitter Cards](https://dev.twitter.com/cards/markup) meta tags specify how pages should look when they are linked to on twitter. If you decide to specify Twitter Card meta information, you must provide the following meta information in the `name` and `content` attributes:
* `twitter:card` is always `summary` for websites.
* `twitter:site` is the @username of the website on twitter.
* `twitter:creator:id` is the twitter user ID of the content creator.
* Information like the the title, the description, and the image default back to Open Graph, so if you have specified Open Graph meta information, there is no need to do that twice.

### Body ###

You can modify the layout in any way you wish; however, it is recommended you use HTML5 tags like `<header>`, `<nav>`, `<section>`, and `<footer>`. They are semantic, and so they are helpful to screen readers and to anyone reading your source code.

For stylistic purposes, using `<div>` is still okay and encouraged.

Avoid using the `<main>` element, however. Internet Explorer 11 and below do not support it, so it is best to use `<section>` elements instead.

### Scripts ###

Put script elements at the bottom of the page so that they don't interfere with the HTML loading.

## CSS ##

### Normalize.css ###

A minified version of normalize.css has been included. To save even more space, you may download another normalize.css and cut out whatever elements are not needed in your project.

### Global ###

All elements have the `box-sizing: border-box` style, which makes creating layouts more intuitive. See [Paul Irish's blog post](http://www.paulirish.com/2012/box-sizing-border-box-ftw/) about it for more information.

Images have a `max-width: 100%` style in order to make them responsive. The size of images will dynamically grow or shrink as the width of the viewport changes.

A `.clearfix` has been included in order to address a common problem caused by floating elements on the page. If you're using floats and your page looks weird, try adding a `.clearfix`.

### Media Queries ###

Feel free to edit the size of the media queries as needed.

## JavaScript ##

jQuery has been included. If not needed, remove.

Place JavaScript in the js/app.js file. However, if it's a tiny bit of code, it may make more sense to place all the code in a `<script>` element in index.html.

## Others ##

You may link fonts in the `<head>`, or store them in a fonts folder and use `@font-face` in the CSS. You decide based on the project.

A favicon.ico is included. Change this as needed based on the project.

If you're using Google Analytics, place the code at the bottom of the `<body>`. Placing it in the `<head>` seems to slow down the page.

Keep your folders organized. If you have PHP code, place it in a php folder. Images should go in an img folder. And so on...