### General 

In Veams-Methodology every `HTML` element gets a class (that is not always possible but we can try it). 

Veams is partially using `BEM`. That is why our class systematic looks like this: 

#### Example Snippet

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

The parent element is `c-article--default`. In general the classes of the child elements consists of the instruments name without any prefix and two `__`.

#### Do not 

Veams-Methodology does not use the following of `BEM`: 

``` html
<article class="c-article" data-css="c-article">
	<header class="article__header">
		<h1 class="article__header__h1">The PG methodology is designed to be used in large, long lived websites and projects.</h1>
		<h2 class="article__header__h2">This is how we make our Sass structure scalable.</h2>
	</header>
	<div class="article__content"></div>
</article>
``` 

**In Veams-Methodology we go only one level deep, because:** 

1. We try to avoid super long class names.
2. For real web applications this is more than enough to handle classes in one instrument.

### Instruments And Prefixing

The class systematic of Veams determines that we have to prefix our instruments (Regions, Components, Utilities). As a result these instruments are very easy to recognize:

1. Regions (`.r-`)
2. Components (`.c-`)
3. Utilities (`.u-`)

> For Utilities prefixes are optional, because many frameworks already provides helper classes. 

### File and Folder Structure

As a result we get a folders structure which is following the: 

**Sass**

``` bash
├── app.scss
├── core
│   └── styles
│       └── base.scss
└── shared
    ├── components
    │   └── article
    │       └── styles
    │           └── _article.scss
    ├── styles
    │   └── layouts
    │       └── _header.scss
    ├── utilities
    │   └── grids
    │       └── styles
    │           └── _grid.scss
``` 

