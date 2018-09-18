[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-12"}})

# Items

> Items are HTML attributes that you use to define event handlers in your markup


### ITEM RESPONSIBILITES
Items have two responsibilities:
1. Bind JavaScript modules to HTML elements. Or, in other words, `data-js-items` are your JavaScript hooks.
1. Enable event data to get passed between markup and modules.

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})
[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

### USING ITEMS
When you use items, you must add a `data-js-item` attribute to your markup.

[//]: #     ({{/wrapWith}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

### EXAMPLE SNIPPET

```html
<a href="#id4" class="c-cta" data-js-item="toggle-close"></a>
```

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})
[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-12"}})

### ADVANTAGES OF USING ITEMS
Using items in your markup make it clear where your JavaScript bindings are. As a result every developer working on the project, whether they are JavaScript developers or not, can easily identify elements that have JavaScript functionality. Also, using items in your markup allows you to avoid using ID's as JavaScript hooks.

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})
