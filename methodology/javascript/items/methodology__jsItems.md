[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-12"}})

# Items

## Items are HTML attributes that help you define event handlers in your markup 


### ITEM RESPONSIBILITES
Items are used to identify event handlers, which results in items having two responsibilities:
1. Bind and element to a view (what does this mean?) --> Items are our JavaScript hooks 
1. Be part of a module (what does this mean?) --> Items contain data that our modules use to deliver their functionality

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})
[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

### IDENTIFYING ITEMS
When we use Items, we add a data-js-item attribute to our markup. 

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

### ADVANTAGES OF USING ITEMS?
Using Items in our markup makes it clear where our JavaScript bindings are. As a result every developer working on the project, whether they are JavaScript developers, or not, can easily identify elements that have JavaScript functionality. Also, using Items in our markup allows us to avoid using ID's as JavaScript hooks.

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})
