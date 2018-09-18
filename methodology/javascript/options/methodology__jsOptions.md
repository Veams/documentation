[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-12"}})

# Options

> Options are a module's settings (e.g. animation length, visibility, etc).

### OPTIONS RESPONSIBILITIES 
Options have two responsibilities:
1. You can use options in your markup to override the options that you define in your module's constructor
1. Options must be written in valid JSON 

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})
[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

### IDENTIFYING OPTIONS and OPTIONS SYNTAX

 When a module has options, you must at add a `data-js-options` attribute to your markup. The value if the attribute `data-js-options` must be an JSON object. You object should be wrapped in single quotes.

 Including data-js-options in our markup helps developers see which constructor options were overrides.
 
 [//]: #     ({{/wrapWith}})
 [//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

 ### EXAMPLE SNIPPET

```html
 <header class="header" data-js-module="sticky" data-js-options='{"myKey": "myValue"}'></header>
```

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})

 [//]: # ({{#wrapWith "grid-row"}})
 [//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-12"}})

### WHAT IS THE ADVANTAGE OF USING OPTIONS?
Having options available in your markup allows you to modify them dynamically via your backend environment.

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})
