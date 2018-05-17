### General 

Because images speak louder than words, here is an image to illustrate Regions:

![alt text](/img/temp/regions.jpg "Regions")

This image makes it clear, that: 

1. Regions are not reusable. 
2. Regions are only defined in your layout files.
3. Regions subdivide your layout.

> This image is actually borrowed from Drupal.org.

### Why do we use Regions?

We separate layout styles from our other instruments (`Components` and `Regions`). The main benefit is drop-in replacement.

In example we can just replace our `logo` (`Component`) and replace it with a `language-switcher` (`Component`) without worrying about layout issues.

#### Example Snippet

``` html
<header class="r-header">
	<div class="header__inner">
        <div class="header-left"></div>
        <div class="header-right"></div>
	</div>
</header>
```

### File and Folder Structure

Every region should be defined in our layout file (in example `lyt-default.hbs` which you can find in your `layouts` directory).

``` bash
src
├── app
│   └── core
│       ├── layouts
│       │   └── lyt-default.hbs
│       └── components
│           └── header
```

### Styles and Sass Structure

For each layout we create a Sass file. In this layout Sass file we define our regions.

``` bash
src
├── app
│   └──shared
│       └── styles
│           └── layouts
│               ├── _header.scss
│               ├── _main.scss
│               └── _footer.scss
```

### Examples of categorized page regions

* Header Region
* Logo Region in Header
* Navigation Region in Header
* Stage Region
* Main Content Region
* Sidebar Region
* Footer Region

#### lyt-default.hbs

``` hbs
<!DOCTYPE html>
<!--[if lt IE 7]>      <html lang="en" class="no-js lt-ie9 lt-ie8 lt-ie7"> <![endif]-->
<!--[if IE 7]>         <html lang="en" class="no-js lt-ie9 lt-ie8"> <![endif]-->
<!--[if IE 8]>         <html lang="en" class="no-js lt-ie9"> <![endif]-->
<!--[if gt IE 8]><!-->
<html lang="en" class="no-js"> <!--<![endif]-->
<head>
    {{#block "metadata"}}
        {{> _metadata }}
    {{/block}}
    {{#block "styles"}}
        {{> _styles }}
    {{/block}}
</head>
<body class="{{bodyclass}}">

    <header class="r-header">
        {{#block "header"}}{{/block}}
    </header>

    <main class="r-main">
        {{#block "main"}}{{/block}}
    </main>

    <footer class="r-footer">
        {{#block "footer"}}{{/block}}
    </footer>

    {{#block "scripts"}}
        {{> _scripts }}
    {{/block}}

</body>
</html>
```


