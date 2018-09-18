
[//]: # ({{#wrapWith "content-section"}})

[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-8"}})

# What is the Veams Methodology?

Veams Methodology refers to how Veams projects are structured and built up for modularity, scalability, and 
maintainability.

Most web development methodologies are only scoped to `HTML` and `CSS`. As a result, they only handle `class 
systematics`. Veams is scoped to `HTML`, `CSS`, and `JavaScript`.

Veams Methodology does not reinvent the wheel. Veams Methodology is based on concepts from BEM, frontend 
development, backend development and extensive feedback from professional web developers.

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})

[//]: # ({{/wrapWith}})
[//]: # ({{#wrapWith "content-section"}})

[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-8"}})

### What differentiates Veams's Methodology from other web development methodologies?

Veams is a methodology that you can apply across your entire frontend stack.

Typical questions which Veams Methodology is answers are:

1. How should you scope and differentiate your`HTML`?
2. How should you bind `JavaScript` to your DOM elements?
3. How should you structure your layouts?
4. How should you write your `CSS` classes?
5. How should you expand your project?

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})

[//]: # ({{/wrapWith}})
[//]: # ({{#wrapWith "content-section"}})

[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-8"}})

### General Overview

#### Instruments To Structure Your Markup

Markup in Veams applications is structured using "instruments". In the context of Veams instruments are tools that 
you will use to structure the pieces of your application into one of three categories:

* [Regions](http://localhost:3000/docs/methodology/instruments/regions/index.html)
* [Components](http://localhost:3000/docs/methodology/instruments/components/index.html)
* [Utilities](http://localhost:3000/docs/methodology/instruments/utilities/index.html)

> Every instrument has a specific purpose and unique attributes. Click the links above to learn more about each 
instrument.

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})

[//]: # ({{/wrapWith}})
[//]: # ({{#wrapWith "content-section"}})

[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-8"}})

#### CSS class writing system

In general, Veams class naming includes the following:

1. BEM similarities to scope styles
2. Prefix usage to differentiate between instruments
3. Global Styles for instruments
4. Modifier and context styles
5. Layout styles with Regions to separate concerns

Despite that Veam's class naming convention is based on BEM -- Veams does not use BEM. Veams uses BEM with restrictions 
how deep your class names should be. To learn more about how Veams flavor of BEM visit the [CSS Introduction](http://localhost:3000/docs/methodology/css/index.html)
Introduction section.

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})

[//]: # ({{/wrapWith}})
[//]: # ({{#wrapWith "content-section"}})

[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-8"}})

#### JavaScript module initialization, module options, and event handling

Veams Methodology uses `data-` attributes to bind JavaScript to DOM elements. It does not use classes to bind JavaScript to DOM elements the. Javascript is bound to DOM elements for three purposes:

* [Module initialisation (`data-js-module`)](http://localhost:3000/docs/javascript/methodology.html)
* [Options handling (`data-js-options`)](http://localhost:3000/docs/javascript/options.html)
* [Event handling (`data-js-item`)](http://localhost:3000/docs/javascript/items.html)

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})
[//]: # ({{/wrapWith}})
