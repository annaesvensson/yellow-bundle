<p align="right"><a href="README-de.md">Deutsch</a> &nbsp; <a href="README.md">English</a> &nbsp; <a href="README-sv.md">Svenska</a></p>

# Bundle 0.9.3

Bundle website files.

<p align="center"><img src="SCREENSHOT.png" alt="Screenshot"></p>

## How to install an extension

[Download ZIP file](https://github.com/annaesvensson/yellow-bundle/archive/refs/heads/main.zip) and copy it into your `system/extensions` folder. [Learn more about extensions](https://github.com/annaesvensson/yellow-update).

## How to bundle website files

This extension bundles and minifies files for a better loading time. Your website may contain multiple CSS and JavaScript files. Usually these will be cached in the browser, but nevertheless each file has to be checked. This is where a file bundler comes in. It looks in the HTML header for included files and replaces them with one single file for CSS and one for JavaScript.

If you don't want that a file is bundled, specify `data-bundle="exclude"` in the HTML header.

## Examples

Website with unbundled CSS and JavaScript files:

```
<!DOCTYPE html>
<html>
<head>
<title>Example page</title>
<link rel="stylesheet" type="text/css" media="all" href="/assets/gallery.css" />
<link rel="stylesheet" type="text/css" media="all" href="/assets/icon.css" />
<link rel="stylesheet" type="text/css" media="all" href="/assets/stockholm.css" />
<script type="text/javascript" defer="defer" src="/assets/gallery-photoswipe.min.js"></script>
<script type="text/javascript" defer="defer" src="/assets/gallery.js"></script>
</head>
<body>
<h1>Hello world</h1>
</body>
</html>
```

Website with bundled CSS and JavaScript files:

```
<!DOCTYPE html>
<html>
<head>
<title>Example page</title>
<link rel="stylesheet" type="text/css" media="all" href="/assets/bundle-dfd1ef8a4c.min.css" />
<script type="text/javascript" defer="defer" src="/assets/bundle-3808f805bc.min.js"></script>
</head>
<body>
<h1>Hello world</h1>
</body>
</html>
```

Website with bundled and unbundled files:

```
<!DOCTYPE html>
<html>
<head>
<title>Example page</title>
<link rel="stylesheet" type="text/css" media="all" href="/assets/bundle-dfd1ef8a4c.min.css" />
<script type="text/javascript" defer="defer" src="/assets/bundle-3808f805bc.min.js"></script>
<script type="text/javascript" defer="defer" data-bundle="exclude" src="/assets/debug.js"></script>
</head>
<body>
<h1>Hello world</h1>
</body>
</html>
```

## Acknowledgements

This extension includes [Minify 1.3.68](https://github.com/matthiasmullie/minify) by Matthias Mullie. Thank you for the good work.

## Developer

Anna Svensson. [Get help](https://datenstrom.se/yellow/help/).
