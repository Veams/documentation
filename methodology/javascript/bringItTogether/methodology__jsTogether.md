[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-12"}})

# JavaScript Best Practices: Bringing It All Together

## Altogether, modules, options, and items form a complete system for managing JavaScript functionality.

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})

[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

###  To the right, you can see what markup looks like when modules, options, and items are used altogether:

[//]: #     ({{/wrapWith}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

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
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-12"}})

As mentioned earlier, one of the main advantages of Veams is how easily other developers can identify important information about a component simply by looking at the markup.

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})

[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

### Modules 

Look at the first line in the example snippet ***(should be figure)*** above for a basic navigation:

[//]: #     ({{/wrapWith}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

```html
<div class="b-navigation" data-js-module="navigation" data-js-options='{"openOnInit": true}'>
```

This line of code has a ```data-js-module```  attribute with the value ```navigation```. Therefore, we know that our navigation has JavaScript functionality that is contained in it's own module also named ```navigation```. 

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})

[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

### Options

Again look at line one from the complete snippet ***(should be figure)*** above.

[//]: #     ({{/wrapWith}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

```html
<div class="b-navigation" data-js-module="navigation" data-js-options='{"openOnInit": true}'>
```

Beside a ```data-js-module``` attribute, line one also has a ```data-js-options``` attribute with the value ```{"openOnInit": true}```. So, on top of knowing that ```navigation``` is module, we also immediately know that this module has an option, we know it's value, and we know that we can override it's value via our frontend, or our backend, environment. 

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})

[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

### Items 

In the large snippet above there are six elements with a ```data-js-item``` attribute

First, our navigation anchors have ```data-js-item```  attributes both with the value ```nav-anchor.```

[//]: #     ({{/wrapWith}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

```html
<a class="navigation__anchorlist-link" role="tab" aria-controls="panel-1" data-js-item="nav-anchor" href="#panel-1">Capital Markets</a>
```

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})

[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

Second, our ```nav```  element has a  ```data-js-item``` attribute with the value ```"nav-container```.

[//]: #     ({{/wrapWith}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

```html
 <nav class="navigation__tabs" data-js-item="nav-container">
```
[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})

[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

Third, our ```li```  elements have ```data-js-item``` attributes both with the value ```nav-panel```. 

[//]: #     ({{/wrapWith}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})
[//]: #     ({{/wrapWith}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})


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
         
```html
<button class="navigation__close" data-js-item="nav-close">Close Navigation</button>
```
[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})

[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

By simply reviewing our markup for ```data-js-items``` we can easily identify which elements have JavaScript functionality. 

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})
