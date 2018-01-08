# [AlphaEdge website](https://alphaedge.io) project

https://alphaedge.io

Branches:
* master
* ae-dev

---

## Jekyll part

Clone/fork the project

Install Jekyll - [Quick start](https://jekyllrb.com/docs/quickstart/)

run `bundle install` & `jekyll serve`

### Mathjax-in-markdown

Use the MathJax delimiters to start and end each formula as follows:

* For centered formulae, use `\\[` and `\\]`.
* For inline formulae, use `\\(` and `\\)`.

source - This [blog post](https://hiltmon.com/blog/2017/01/28/mathjax-in-markdown/)

add `math: true` to front-matter to add Mathjax Script to the page

### Highlight with Rouge

`{% highlight python %}
x = ('a', 1, False)
{% endhighlight %}`


### Add lightbox feature to image in Markdown

use `{: data-lightbox="true"}`

```markdown
[![Alt text](http://via.placeholder.com/900x400)](http://via.placeholder.com/1800x800){: data-lightbox="true"}
```

source - This [blog post](https://kramdown.gettalong.org/quickref.html)

### Add classes to images in markdown

example:

```markdown
![Alt text](http://via.placeholder.com/848x565){: class="img-responsive border--round"}
```

---

### Collections and posts

1. Trading Software Solutions
   - Live Trading
   - Portfolio management
   - Portfolio Backtest
   - Risk Analysis
2. Trading Strategies
   - Mean Reversion
     - Mean Variance Optimizer
   - Portfolio optimisation
   - Momentum
     - Protective Asset momentum
   - Technical analysis
   - Volatility
3. Docs
   - User Guide
   - Developer Guide
   - Framework API
   - Tutorials
4. Support
   - Community Forum
   - Contact Support
5. Blog
   - Posts (blog/post-title)
  
---

### Spacing

set class for spacing of the proper item in `_data/spacing.yml`
```
spacing-class: space--sm, space--lg etc.
page-title-spacing-class: space--sm
sidebar-spacing: '' - no class, boxed--sm, boxed--lg etc.
```

### Sitemap

Loops through the posts, pages and collections (strategies, solutions, documentation)

### Responsive images

#### Device's
* *widths*: 1440 - 1024 - 768 - 320
* *ppi*: 1.0 - 2.0

#### Images:

Thumbnails
555x370 - 455x303 - 345x230 - 290x193

---

In solutions & recent posts
360x240 - 293x196 - 220x147 - 290x193

---

In strategy items 
848x565 - 698x465 - 720x480 - 290x193

---

Blog items-thumbnails
360x240 - 293x196 - 345x230 - 290x193

---

Blog post images
750x500 - 617x411 - 720x480 - 290x193

---

Picture tag syntax: `{% picture preSet image.jpg alt="Alt" %}`


Example generated: 

```html
<picture>
    <source srcset="~path~to~/insurance-2-1110by740-6f25b0.jpg" media="(min-width: 1440px) and (-webkit-min-device-pixel-ratio: 2), (min-width: 1440px) and (min-resolution: 192dpi)">
    <source srcset="~path~to~/insurance-2-555by370-6f25b0.jpg" media="(min-width: 1440px)">
    <source srcset="~path~to~/insurance-2-910by607-6f25b0.jpg" media="(min-width: 1024px) and (-webkit-min-device-pixel-ratio: 2), (min-width: 1024px) and (min-resolution: 192dpi)">
    <source srcset="~path~to~/insurance-2-455by303-6f25b0.jpg" media="(min-width: 1024px)">
    <source srcset="~path~to~/insurance-2-690by460-6f25b0.jpg" media="(min-width: 768px) and (-webkit-min-device-pixel-ratio: 2), (min-width: 768px) and (min-resolution: 192dpi)">
    <source srcset="~path~to~/insurance-2-345by230-6f25b0.jpg" media="(min-width: 768px)">
    <source srcset="~path~to~/insurance-2-580by387-6f25b0.jpg" media="(min-width: 320px) and (-webkit-min-device-pixel-ratio: 2), (min-width: 320px) and (min-resolution: 192dpi)">
    <source srcset="~path~to~/insurance-2-290by193-6f25b0.jpg" media="(min-width: 320px)">
    <source srcset="~path~to~/insurance-2-1110by740-6f25b0.jpg" media="(-webkit-min-device-pixel-ratio: 2), (min-resolution: 192dpi)">
    <source srcset="~path~to~/insurance-2-555by370-6f25b0.jpg">
    <img src="~path~to~/insurance-2-555by370-6f25b0.jpg" class="border--round box-shadow-wide" itemprop="image" alt="Insurance">
</picture>
```