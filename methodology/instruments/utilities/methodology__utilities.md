[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

# Utilities

Most applications have markup that has no relationship to its content but is important to display the inner HTML in a structured way. Good examples are the grid helper classes that Foundation and Boostrap provide.

To achieve the same goal, Veams provides a `Utility` instrument and powerful set of [Handlebars helper](/veams-cli/template-helper/overview.html#wrapwith-helper-block-helper-).
 
Examples Utilities are:

1. Grid systems classes
2. Multiple sections in regions

> Note: You do not have to use Utilities if you think it's not necessary. It's totally up to you.

### Why use Utilities?

Utilities simplify the differentiation between `Components` and helper markup.

[//]: #     ({{/wrapWith}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})



[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})

[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})


### Example Utlility: Grid System


[//]: #     ({{/wrapWith}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

### Grid System

``` html
<div class="u-grid-row">
    <div class="u-grid-col is-3">
    </div>
    <div class="u-grid-col is-3">
    </div>
    <div class="u-grid-col is-3">
    </div>
</div>
```

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})

[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

### Example Utility: Grid Row and Grid Column Classes

[//]: #     ({{/wrapWith}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

#### Grid Row Class

``` hbs
<div class="u-grid-row{{#unless props.padding}} is-collapsed{{/unless}}{{#if props.classes}} {{props.classes}}{{/if}}">
	{{{yield}}}
</div>
```

#### Grid Column

``` hbs
<div class="u-grid-col{{#if props.colClasses}} {{props.colClasses}}{{/if}}">
	{{{yield}}}
</div>
```

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})


