[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

# Regions

Regions are sections of HTML that are used to structure your web pages. More specifically:

1. Regions are not reusable. 
2. Regions are only used in your layout files.
3. The purpose of regions are to segment your layout.

Of the three instruments that Veams uses, regions are the highest-level instrument. Regions contain components.

The diagram below illustrates how regions are used to section a page and contain components:

![alt text](/img/temp/regions.jpg "Regions")

> This image is borrowed from Drupal.org.

### Why use Regions?

Regions allow you to separate your layout styles from other instrument's styles (`Components` and `Regions`). The main benefit of separating styles is drop-in replacement.

For example, in the sample code, by separating layout styles from component styles, you can swap the `logo` component with the `language-switcher` component and you don't have to worry about breaking your layout.

### Examples of page regions are:

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

Every region should be defined in our layout file (in example `lyt-default.hbs`. You can find your layout files in your `layouts` directory).

For each layout you should create a Sass file. In this layout Sass file you will define your regions.


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
