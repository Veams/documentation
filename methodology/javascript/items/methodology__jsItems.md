[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-12"}})

# Items

## Items are HTML attributes that you use to define event handlers in your markup


### ITEM RESPONSIBILITES
Items have two main responsibilities:
1. Bind and element to a view (what does this mean?) --> Items are our JavaScript hooks?
1. Be part of a module (what does this mean?) --> Items contain data that our modules use to deliver their functionality?

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})
[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

### IDENTIFYING ITEMS
When you use items, you add a `data-js-item` attribute to your markup.

[//]: #     ({{/wrapWith}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

```html
<a href="#id4" class="c-cta" data-js-atom="toggle-close"></a>

cta.hbs
```

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})
[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-12"}})

### ADVANTAGES OF USING ITEMS
Using items in your markup make it clear where your JavaScript bindings are. As a result every developer working on the project, whether they are JavaScript developers or not, can easily identify elements that have JavaScript functionality. Also, using items in your markup allows you to avoid using ID's as JavaScript hooks.

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})
