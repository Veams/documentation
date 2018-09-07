[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-12"}})

# Global Styles

## Global styles refers to css styles that Veams instrument's share.

### Veams instruments share styles via the `data-css` attribute. 


[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})

[//]: # ({{#wrapWith "grid-row"}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

#### General Principles

- Global styles are shared by all of your instrument's contexts.

- If your instrument needs global styles, use the `data-css` attribute in your markup. 

- Your global styles should live in the `data-css` rule in your instrument's style sheet.

Note: Using the `data-css` attribute has no advantage over using SCSS `mixins` or `extends`. However, using `data-css` does make your global styles easier to identify because they are visible in your markup.

[//]: #     ({{/wrapWith}})
[//]: #     ({{#wrapWith "grid-col" colClasses="is-col-mobile-l-6"}})

### Example Snippet

``` html
<article class="c-article--default" data-css="c-article"></article>
```

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
		display: flex;
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
		justify-content: center;
		margin-bottom: 3rem;
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
		justify-content: flex-start;
		margin-bottom: 2rem;
	}
```

[//]: #     ({{/wrapWith}})
[//]: # ({{/wrapWith}})
