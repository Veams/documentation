# Modules

## Modules to define individual, segmented, pieces of  JavaScript functionality. Each module is self-contained unit with it's own file and directory. 

---

### MODULE RESPONSIBILITIES
Veams modules have two responsibilites: 
1. Initialization 
1. Module Option Handling 
Tip: Module initialization is... **(insert what module initialization means in plain english)**. Options are a module's settings (e.g. animaton length, visibility). Modules have default options. Default options can be overwritten via the components JSON data file.

---

### IDENTIFYING MODULES 
When bind modules to our markup via the ****data-js-module**** attribute. The purpose of data the data-js-module attribute is to help developers easily identify elements that have JavaScript functionality. 

```html
<header class="header" data-js-module="sticky"></header>

header.hbs 
```
