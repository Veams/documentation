[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

### General

Components are reusable HTML snippets. That means, one page can display multiple identical Components with different data. 

1. Components always closely related to content.
2. Components content is a variable and can change on different contexts/pages.
3. Components generic and can be used all over your project.
4. Components can contain Components.

### Why do we use Components?

Because of reusability. With reusability you can build building block libraries (we had, see [Veams-Components](/veams-components/index.html)).

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

When you use a Templating Engine, it is important to create a folder for your components. Each component gets its own folder.

[//]: #     ({{/wrapWith}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

Example of Component folder structure:

``` bash
├── components
    └── article
        ├── data
        │   └── article.hjson
        ├── styles
        │   └── _article.scss
        ├── templates
        │   ├── article-usage.hbs
        │   ├── article.hbs
        │   ├── article__header.hbs
        │   └── article__footer.hbs
        ├── article-usage.settings.hjson
        └── README.md
```

[//]: #     ({{/wrapWith}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

To structure sub elements of a Component for example `<header>` in an `<article>`, we create a new partial and define the name (like BEM: `article__header.hbs`).

[//]: #     ({{/wrapWith}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

Example of the header inside the `article.hbs`

``` hbs
{{#if options.content.articleHeader}}
    <header class="article__header{{#if options.settings.articleHeaderClasses}} {{options.settings.articleHeaderClasses}}{{/if}}">
        {{> article__header options.content.articleHeader}}
    </header>
{{/if}}
```

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})




