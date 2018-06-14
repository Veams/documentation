# Options

## Options are a module's settings (e.g. animaton length, visibility). 
---

### OPTIONS RESPONSIBILITIES 
Options have two responsibilities:
1. Overriding options that we define in the module's constructor
Providing us a valid JSON format  **Question: What does this mean and why does it matter?**

---

### IDENTIFYING OPTIONS

 When a module has options, we add a data-js-option to markup. Including data-js-option in our markup helps developers see option overrides. 
 
```html
 <header class="header" data-js-module="sticky" data-js-options='{"myKey": "myValue"}'></header>
 
 header.hbs 
```

---
 
### OPTIONS SYNTAX
We use a single quotation mark to wrap our JSON string (see the example code snippet above).

---

### WHAT IS THE ADVANTAGE OF USING OPTIONS?
Options in our markup allows us to control our module's options via our backend environment.
