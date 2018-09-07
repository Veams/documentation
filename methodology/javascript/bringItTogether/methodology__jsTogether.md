[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-12"}})

# Bringing It All Together

## Altogether, modules, options, and items form a complete system for managing JavaScript functionality.

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})

[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

###  To the right, you can see an example of what markup looks like when modules, options, and items are used altogether. The example markup for a basic navigation.

[//]: #     ({{/wrapWith}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

### EXAMPLE SNIPPET

```html
<div class="b-navigation" data-js-module="navigation" data-js-options='{"openOnInit": true}'>
    <h2 class="navigation__headline is-hidden">Navigation</h2>
    <ol class="navigation__anchorlist" role="tablist">
        <li class="navigation__anchorlist-item">
            <a class="navigation__anchorlist-link" role="tab" aria-controls="panel-1" data-js-item="nav-anchor" href="#panel-1">Capital Markets</a>
        </li>
        <li class="navigation__anchorlist-item">
            <a class="navigation__anchorlist-link" role="tab" aria-controls="panel-2" data-js-item="nav-anchor" href="#panel-2">Retail Banking</a>
        </li>
    </ol>

    <nav class="navigation__tabs" data-js-item="nav-container">
        <ul class="navigation__tablist">
            <li id="panel-1" role="tabpanel" aria-hidden="true" class="navigation__tab" data-js-item="nav-panel">
                <section class="navigation__tab-inner"></section>
            </li>

            <li id="panel-2" role="tabpanel" aria-hidden="true" class="navigation__tab" data-js-item="nav-panel">
                <section class="navigation__tab-inner"></section>
            </li>
        </ul>
        <button class="navigation__close" data-js-item="nav-close">Close Navigation</button>
    </nav>
</div>
```
[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})

[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-12"}})

### As previously mentioned, one of the main advantages of Veams is how easily developers can identify important information about components by looking at markup. Below we deconstruct the code block above to demonstrate how you can get information about a component's JavaScript functionality by reviewing it's markup.

[//]: #     ({{/wrapWith}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

### Modules 

The line of code to the right is first line of code from the code block above.

This line of code has a ```data-js-module```  attribute with the value ```navigation```. Based on this information you know that the navigation has JavaScript functionality that is defined in a module named ```navigation```.

[//]: #     ({{/wrapWith}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

### EXAMPLE SNIPPET

```html
<div class="b-navigation" data-js-module="navigation" data-js-options='{"openOnInit": true}'>
```

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})

[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

### Options

To the right again there is the first line from the whole snippet above.

Beside a ```data-js-module``` attribute, the line also has a ```data-js-options``` attribute with the value ```{"openOnInit": true}```. So, on top of knowing that ```navigation``` is module, you can also infer that this module has an option, you know it's name, it's value, and you know that you can override it's value via your backend environment.

[//]: #     ({{/wrapWith}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

### EXAMPLE SNIPPET

```html
<div class="b-navigation" data-js-module="navigation" data-js-options='{"openOnInit": true}'>
```

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})

[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

### Items 

It's not uncommon for complicated components to have multiple `data-js-item` attributes. For example, the navigation snippet above has six elements with a ```data-js-item``` attributes:

First, the navigation anchors have ```data-js-item```  attributes both with the value ```nav-anchor.```

[//]: #     ({{/wrapWith}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

### EXAMPLE SNIPPET

```html
<a class="navigation__anchorlist-link" role="tab" aria-controls="panel-1" data-js-item="nav-anchor" href="#panel-1">Capital Markets</a>
```

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})

[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

Second, the ```nav```  element has a  ```data-js-item``` attribute with the value ```"nav-container```.

[//]: #     ({{/wrapWith}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

### EXAMPLE SNIPPET

```html
 <nav class="navigation__tabs" data-js-item="nav-container">
```
[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})

[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

Third, the ```li```  elements have ```data-js-item``` attributes both with the value ```nav-panel```.

[//]: #     ({{/wrapWith}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

### EXAMPLE SNIPPET

```html
<li id="panel-1" role="tabpanel" aria-hidden="true" class="navigation__tab" data-js-item="nav-panel">
  <section class="navigation__tab-inner"></section>
</li>
```
[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})
[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

Finally the navigation's close button is a ```data-js-item``` attribute with the value ```nav-close```.
 
[//]: #     ({{/wrapWith}})      
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

### EXAMPLE SNIPPET

```html
<button class="navigation__close" data-js-item="nav-close">Close Navigation</button>
```
[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})

[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

The main point to remember about ```data-js-items``` is you use them identify bind JavaScript functionality to elements and you can use them identify which elements in Veams projects have JavaScript functionality.

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})
