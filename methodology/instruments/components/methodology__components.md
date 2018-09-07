[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-12"}})

# Components

Components are reusable HTML snippets. One page can display multiple components with different content.

1. Components are always closely related to content.
2. Component's content are variables and can change in different contexts.
3. Components are generic and can be used all over your project.
4. Components can contain other components.

### Why should you use components?

The main reason you should use components is reusability. Reusability allows you to drop components into your pages and not only will they just work, they will look they way were designed to look.

Veams already has a library of components. You can install via npm and snap them together like legos to quickly build pages.

Examples of ready-to-us Veams components include:

- article - Articles can be used in teasers or on pages, content sections and so on.
- figure - Figures can be placed in an article or teaser or carousel.
- picture - Pictures can be placed in figures.
- teaser - When we use teasers in sliders and other modules and the content is flexible then we define it as component.
- list-item

To learn more about Veam's component library, see [Veams-Components](/veams-components/index.html)).

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})
[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

### Component Structure

You should prefix your components with c- (or _c- for Sass files).

[//]: #     ({{/wrapWith}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

```html
<article class="c-article--default" data-css="c-article--default"></article>
```

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})
[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

#### Example Component: Figure

[//]: #     ({{/wrapWith}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

#### Figure Component

```hbs
<figure \{{#if figureId}}id="\{{figureId}}" \{{/if}}class="c-figure\{{#if figureContextClass}}--\{figureContextClass}}\{{/if}}\{{#if figureClasses}} \{{figureClasses}}\{{/if}}" data-css="c-figure">
    <div class="figure__wrapper">
        \{{#if pictureUrlStd}}
            \{{> c-picture}}
        \{{else}}\{{#if video}}
            \{{> c-video}}
        \{{/if}}\{{/if}}
    </div>
    \{{#if figureCaption}}
        <figcaption class="figure__caption\{{#if figureCaptionClasses}} \{{figureCaptionClasses}}\{{/if}}">
            \{{> c-figure__caption figureCaption}}
        </figcaption>
    \{{/if}}
</figure>


```

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})




