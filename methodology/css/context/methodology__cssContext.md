[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-12"}})

# Contexts

## Instead of duplicating components with different styles, you should create new `contexts`. `Contexts` are variations of components that share a base set of styles and have their own context-specific styles.

> Contexts make your components more modular and reusable. 


[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})
[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})


#### General Principles

- To create a new context Veams uses two dashes and a name after the instrument's prefix to identify the new
context `.c-name--context`. 

- Context styles are completely independent from other styles and should never override the global `data` attribute 
styles of the instrument.

- The main purpose of contexts is to allow components to share styles where it makes sense while still having 
independent styles that allow the component to be reused in different contexts.

- Contexts also make it easy to determine which context is rendered by inspecting a page's markup.

[//]: #     ({{/wrapWith}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

### Example "default" context markup 

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

### Example "microsite" context markup

``` html
<article class="c-article--microsite is-bg-dark" data-css="c-article">
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

### Example SCSS file for both contexts ("default" and "microsite")

#### _article.scss

``` scss
/* ===================================================
ARTICLE COMPONENT
=================================================== */

/* 
Global Styles
 */
[data-css="c-article"] {
	/*
	Header
	-- */
	.article__header {
	}

	.article__header-time {
	}

	.article__header-headline {
	}

	.article__header-subline {
	}

	.article__header-intro {
	}

	/*
	Content
	-- */
	.article__content {
	}

	/*
	Footer
	-- */
	.article__footer {
	}

	.article__footer-link {
	}
}


/* 
Context: Default 
 */
.c-article--default {
	/*
	Header
	-- */
	.article__header {
		margin-bottom: 3rem;
	}

	.article__header-time {
		font-size: 1.2rem;
	}

	.article__header-headline {
		font-size: 2.8rem;
		margin-bottom: 1.15rem;
	}

	.article__header-subline {
		font-size: 2.2rem;
		margin-bottom: .75rem;
	}

	.article__header-intro {
		font-size: 2rem;
		font-weight: 900;
	}

	.article__footer {
		margin-top: 3rem;
	}
}

/* 
Context: Microsite 
 */
.c-article--microsite {
	/*
	Header
	-- */
	.article__header {
		margin-bottom: 2rem;
	}

	.article__header-time {
		font-size: 1.1rem;
	}

	.article__header-headline {
		font-size: 2.5rem;
		margin-bottom: 1.25rem;
	}

	.article__header-subline {
		font-size: 2rem;
		margin-bottom: 1rem;
	}

	.article__header-intro {
		font-size: 2.5rem;
		font-weight: 900;
	}

	.article__footer {
		margin-top: 2rem;
	}
}
```
[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})
