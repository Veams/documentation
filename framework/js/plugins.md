[//]: # ({{#wrapWith "content-section"}})

[//]: #     ({{#wrapWith "grid-row"}})
[//]: #         ({{#wrapWith "grid-col" colClasses="is-col-tablet-l-8"}})

# Plugins in `VEAMS`

In general the plugin system in `VEAMS` is a really simple one. 

------------- 

## Usage of a plugin

When you want to use a plugin you first need to import the plugin and then just execute the `use` method of `VEAMS`: 

```js
import PluginXY from 'PluginXY';

// Add plugins to the Veams system
Veams.use(PluginXY);
```

You can pass in options to the plugin just by adding other parameters:

```js
import PluginXY from 'PluginXY';

// Add plugins to the Veams system
Veams.use(PluginXY, {
	// Options object
    my: 'option'
});
```

------------- 

## Creation of plugins

When you want to create a plugin you only need to export an object with an `initialize` method in it. It is really easy. 

Let's say you want to add jQuery as DOM handler in `VEAMS` and want to share one single instance in the project: 

1. First you need to import the jQuery library
2. Then you create a simple object 
    - The `pluginName` is optional
    - Into the `initialize` method there will be passed the `VEAMS` object
3. Execute `use` of `VEAMS`.

```js
import $ from 'jquery';

const DomPlugin = {
  pluginName: '$',
  initialize: function(Veams) {
    Veams.$ = $;
  }
};

Veams.use(DomPlugin);
```

That's it. You extended the general `VEAMS` object. Now you can just work with this instance by accessing it: 

``` js
import Veams from './app.js';

Veams.$('.page-wrapper').addClass('is-working');
```

------------- 

## Available plugins

There are multiple plugins available.

Please keep in mind that the order of the initialisation of your used plugins can be important. In general it makes sense to use the following order: 

``` js
// Intialize core of Veams
Veams.onInitialize(() => {
	Veams.use(VeamsLogger);
	Veams.use(VeamsVent); // VeamsVent enhances VeamsModules and VeamsMediaQueryHandler
	Veams.use(VeamsMediaQueryHandler);
	Veams.use(VeamsModules);
});
```

[//]: #         ({{/wrapWith}})
[//]: #     ({{/wrapWith}})

[//]: # ({{/wrapWith}})
