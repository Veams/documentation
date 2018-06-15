[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

### What are Regions?

Because images speak louder than words, here is an image to illustrate Regions:

![alt text](/img/temp/regions.jpg "Regions")

{{!debug this}}

This image makes it clear, that: 

1. Regions are not reusable. 
2. Regions are only defined in your layout files.
3. Regions subdivide your layout.

> This image is actually borrowed from Drupal.org.

### Why do we use Regions?

We separate layout styles from our other instruments (`Components` and `Regions`). The main benefit is drop-in replacement.

In example we can just replace our `logo` (`Component`) and replace it with a `language-switcher` (`Component`) without worrying about layout issues.

### Examples of categorized page regions

* Header Region
* Logo Region in Header
* Navigation Region in Header
* Stage Region
* Main Content Region
* Sidebar Region
* Footer Region
            
[//]: #     ({{/wrapWith}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

#### One Region in HTML

``` html
<header class="r-header">
    <div class="header__inner">
        <div class="r-header-left"></div>
        <div class="r-header-right"></div>
    </div>
</header>
```

#### Handlebars Layout Example

``` hbs
<!DOCTYPE html>
<!--[if lt IE 7]>      <html lang="en" class="no-js lt-ie9 lt-ie8 lt-ie7"> <![endif]-->
<!--[if IE 7]>         <html lang="en" class="no-js lt-ie9 lt-ie8"> <![endif]-->
<!--[if IE 8]>         <html lang="en" class="no-js lt-ie9"> <![endif]-->
<!--[if gt IE 8]><!-->
<html lang="en" class="no-js"> <!--<![endif]-->
<head>
    \{{#block "metadata"}}
        \{{> _metadata }}
    \{{/block}}
    \{{#block "styles"}}
        \{{> _styles }}
    \{{/block}}
</head>
<body class="\{{bodyclass}}">

    <header class="r-header">
        \{{#block "header"}}\{{/block}}
    </header>

    <main class="r-main">
        \{{#block "main"}}\{{/block}}
    </main>

    <footer class="r-footer">
        \{{#block "footer"}}\{{/block}}
    </footer>

    \{{#block "scripts"}}
        \{{> _scripts }}
    \{{/block}}

</body>
</html>
```
	
[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})
[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

### File and Folder Structure

Every region should be defined in our layout file (in example `lyt-default.hbs` which you can find in your `layouts` directory).

For each layout we create a Sass file. In this layout Sass file we define our regions.


[//]: #     ({{/wrapWith}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

``` cmd
src
└── app
   └── core
       └── layouts
           |── lyt-default.hbs
           └── lyt-default.scss
```

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})
