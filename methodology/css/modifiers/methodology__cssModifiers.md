[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-12"}})

# Modifiers

## Modifiers classes are used to make small changes to the appearance of instruments. 

### Modifiers are useful when instrument customizations are small enough not to require creating a new context.

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})

[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

#### General Principles

The the example to the right shows the usage of a modifier (`.is-active`) on a navigation element:
               
- A modifier change is a small change. This could be a different background color, float direction or font-size. 

- You should declare modifier rules with `.is-` or `.isnt-`. 

- Modifier changes should only change a small part of it's context.

[//]: #     ({{/wrapWith}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

### Example Modifier Snippet

Example modifier class ("is-active") on a navigation element:

``` html
<nav class="b-navbar" id="site-menu">
    <h2>Templating in PG</h2>
    <ul class="navbar__list">
        <li class="navbar__list-item">
            <a class="navbar__link" href="../templating-in-pg/template-overview.html">Assemble Overview</a>
        </li>
        <li class="navbar__list-item">
            <a class="navbar__link is-active" href="../templating-in-pg/template-layouts.html">Assemble Standard Layouts</a>
        </li>
        <li class="navbar__list-item">
            <a class="navbar__link" href="../templating-in-pg/template-layouts--extended.html">Assemble Extended Layouts</a>
        </li>
    </ul>
</nav>
```
 
 [//]: #     ({{/wrapWith}})
 [//]: # ({{/wrapWith}})
