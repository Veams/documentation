[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-12"}})

# Modules

> Modules define individual, segmented, pieces of JavaScript functionality. Each module is a self-contained unit with it's own file and directory.

[//]: #     ({{/wrapWith}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-12"}})

### MODULE RESPONSIBILITIES
Veams modules have two responsibilites: 
1. Initialization
1. Module option handling

Reminder: Module initialization is how you connect components to modules. Options are a module's settings (e.g. animaton length, visibility). Modules often have default options. A module's default options can be overwritten via the component's JSON file.

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})

[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

### IDENTIFYING MODULES 
In Veams projects you bind modules to your markup via the ****data-js-module**** attribute. The purpose of data the data-js-module attribute is to help developers easily identify which elements have JavaScript functionality.

[//]: #     ({{/wrapWith}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

### EXAMPLE SNIPPET

```html
<header class="header" data-js-module="sticky"></header>
```
[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})
