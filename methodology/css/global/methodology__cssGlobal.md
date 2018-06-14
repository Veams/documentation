# CSS: Global Styles

## Global styles refer to Veams instrument's shared styles.

### Veams instruments share styles via the `data-css` attribute. 
---

#### General Principles

- Global styles are shared by all of your instrument's contexts.

- If your instrument needs global styles, use the `data-css` attribute in your markup. 

- Your global styles should live in the `data-css` rule in your instrument's style sheet.

### Example Snippet

``` html
<article class="c-article--default" data-css="c-article"></article>
```

``` scss
/* ===================================================
ARTICLE COMPONENT
=================================================== */

/* ---------------------------------------------------
Global Styles
--------------------------------------------------- */
[data-css="c-article"] {

	/*
	Header
	----------------------- */
	.article__header {
		display: flex;
	}
}


/* ---------------------------------------------------
Context: Default 
--------------------------------------------------- */
.c-article--default {

	/*
	Header
	----------------------- */
	.article__header {
		justify-content: center;
		margin-bottom: 3rem;
	}
}

/* ---------------------------------------------------
Context: Microsite 
--------------------------------------------------- */
.c-article--microsite {

	/*
	Header
	----------------------- */
	.article__header {
		justify-content: flex-start;
		margin-bottom: 2rem;
	}
```

Using global styles does not have a significant advantage over using SCSS `mixins` or `extends`. However, global 
styles are do make your global styles more clear by declaring themselves in your markup via the `data-css` attribute.
