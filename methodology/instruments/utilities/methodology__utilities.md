### General

On most applications we have markup which has no relationship to its content but is important to display the inner HTML in a structured way. Nice examples are grid helper classes like Foundation or Boostrap provides. 

Therefore Veams uses the instrument `Utility` and provides a neat [handlebars helper](/veams-cli/template-helper/overview.html#wrapwith-helper-block-helper-).
 
Examples are:

1. Grid systems per class
2. Multiple sections in regions

> You do not have to use Utilities when you think it is not necessary - this is up to you.

### Why do we use Utilities?

We use Utilities to simplify the differentiation between `Components` and helper markup.

#### Example Snippet

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

### Examples of utlilities: 

* Grid System


### File and Folder Structure

When you use a Template Engine, it is important to create a folder for your utilities. 

Our utilities folder structure can look like this: 

``` bash
src
├── app
│   └──shared
│       └── utilities
│           └── grid
│               ├── data
│               │   └── grid.hjson
│               ├── styles
│               │   └── _grid.scss
│               ├── templates
│               │   ├── grid-usage.hbs
│               │   ├── grid-col.hbs
│               │   └── grid-row.hbs
│               ├── grid.settings.hjson
│               └── README.md
```

#### Grid Row

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
