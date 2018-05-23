### General 

Components are reusable HTML snippets. That means, one page can display multiple identical Components with different data. 

1. Components always closely related to content.
2. Components content is a variable and can change on different contexts/pages.
3. Components generic and can be used all over your project.
4. Components can contain Components.

### Why do we use Components?

Because of reusability. With reusability you can build building block libraries (we had, see [Veams-Components](/veams-components/index.html)).

### File and Folder Structure

When you use a Templating Engine, it is important to create a folder for your components. Each component gets its own folder.

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

To structure sub elements of a Component for example `<header>` in an `<article>`, we create a new partial and define the name (like BEM: `article__header.hbs`).

Example of the header inside the `article.hbs`

``` hbs
{{#if options.content.articleHeader}}
    <header class="article__header{{#if options.settings.articleHeaderClasses}} {{options.settings.articleHeaderClasses}}{{/if}}">
        {{> article__header options.content.articleHeader}}
    </header>
{{/if}}
```






