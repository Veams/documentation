[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-12"}})

# CSS: Introduction

## The section outlines how to Veams to write CSS classes for clarity, maintainability, scalability. 

### Veams uses BEM-style class naming with Regions, Components, and Utilities. 

### Despite using BEM style class names, Veams class naming have a few notable differences to BEM.

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})
[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

#### General principles

- Every `HTML` element get a class. You should write your class names using the `BEM` style class naming convention. 

- If implemented correctly, your classes should have a structure similar to the example snippet below.

In the example above, note that the parent element has a the class`c-article--default`. The prefix `c` indicates that
the element is a component. 

All parent elements are prefixed with a letter the tells developer what the element is. Veams has three 
prefixes:

- Regions are prefixed with the letter `"r"`. 

- Components are prefixed with the letter `"c"`. 

- Utilities are prefixed with the letter `"u"`

> For Utilities prefixes are optional, because many frameworks already provides helper classes.

In line with BEM's class naming convention child elements in Veams projects should have two parts, the region, 
component, or utilities name followed by two underscores `__` and brief description of what the element is. For 
example: 

`article__header`

`overlay__close-button`

`teaser__icon`

`teaser__icon-text`

[//]: #     ({{/wrapWith}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

#### Example snippet

``` html
<article class="c-article--default is-bg-higlight-1" data-css="c-article">
	<header class="article__header is-header">
		<time class="article__header-time" datetime="">11/16/2016</time>
		<h1 class="article__header-headline">Article Headline</h1>
		<h2 class="article__header-subline">Article Subline</h2>
		<p class="article__header-intro">This is an intro text which can be used in every article component.</p>
	</header>
	<div class="article__content is-visible">
		Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam aperiam architecto atque cupiditate dicta earum ex facilis harum incidunt, laboriosam officiis placeat quas recusandae, rerum, sit tempore tenetur. Impedit, velit.
	</div>
	<footer class="article__footer is-margin">
		<a class="article__footer-link" href="#">Footer Link in Article</a>
	</footer>
</article>
``` 

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})
[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

#### How Veams class naming is different when compared to BEM.

Your class names should only be one level deep (i.e. only have one underscore-separated section). There are two reason 
for this:

1. For improved readability, you should avoid very long class names.
2. For most web applications a single level of depth is sufficient to target a parent instrument and it's child 
elements.

Therefore, when using Veams, you should not have class names that have more than one underscore-separated section. 
For example:  

[//]: #     ({{/wrapWith}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

**Do Not**

``` html
<article class="c-article" data-css="c-article">
	<header class="article__header">
		<h1 class="article__header__h1">The PG methodology is designed to be used in large, long lived websites and projects.</h1>
		<h2 class="article__header__h2">This is how we make our Sass structure scalable.</h2>
	</header>
	<div class="article__content"></div>
</article>
``` 

**Do**

``` html
<article class="c-article" data-css="c-article">
	<header class="article__header">
		<h1 class="article__header-h1">The PG methodology is designed to be used in large, long lived websites and 
		projects.</h1>
		<h2 class="article__header-h2">This is how we make our Sass structure scalable.</h2>
	</header>
	<div class="article__content"></div>
</article>
``` 

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})
