[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

### General

Components are reusable HTML snippets. One page can display multiple identical Components with different data.

1. Components are always closely related to content.
2. Component's content are variables and can change in different contexts.
3. Components are generic and can be used all over your project.
4. Components can contain other components.

### Why you should we use components?

The main reason to use components is reusability. Reusability allows you drop components into your pages and not only will they just work, they will look they way were designed, too.

Veams has a library of components. You can install them and snap them together like legos to quickly build pages.

To learn more about Veam's component library, see [Veams-Components](/veams-components/index.html)).

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

When you use components, it's important organize them properly. Veams components live in the "components" directory. Within the "components" directory, each component gets its own folder where it's markup, stylesheets, and script files live.

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

You can subdivide components using "partials." To structure sub elements of a component and define it. For example, to put a header `<header>` in an `<article>`, the naming using Veam's BEM-style naming convention could be `article__header.hbs`.

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




