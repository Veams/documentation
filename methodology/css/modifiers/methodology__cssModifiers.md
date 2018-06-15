# CSS: Modifiers

## Modifiers classes are used to make small changes to the appearance of instruments. 

### Modifiers are useful when instrument customizations are small enough not to require creating a new context.
---

#### General Principles

The following example shows you the usage of a modifier (`.is-active`) on a navigation element: 
               
- A modifier change is a small change. This could be a different background color, float direction or font-size. 

- You should declare modifier rules with `.is-` or `.isnt-`. 

- Modifier changes should only change a small part of it's context.

### Example Modifier Snippet

The following example shows the use of a several modifier classes on an article element: 

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

The parent element `c-article--default` has the modifier class `is-bg-higlight-1`. The child element `article__content`has
the modifier class `is-visible`. Finally, the child element `article__footer` has the modifier class `is-margin`.
 
 
