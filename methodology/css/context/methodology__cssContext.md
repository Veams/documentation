### General

To add a context we use two dashes like `.c-name--context`. Context styles are completely independent from other styles and should never override our global `data` styles of the instrument.

### Example HTML output

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

### What is the advantage to use a context? 

Context styles are scoped. They are a complete independent style for an instrument (Component). Therefore we do not have any inheritance problems.

### Example

A Sass file can look like this: 

#### _article.scss

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
	----------------------- */
	.article__content {
	}

	/*
	Footer
	----------------------- */
	.article__footer {
	}

	.article__footer-link {
	}
}

/* ---------------------------------------------------
Context: Default Example
--------------------------------------------------- */
.c-article--default {
	/*
	Header
	----------------------- */
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

```
