# An Exhibition of a Hunger Artist

Here is the blog of WHY: [https://einhungerkuenstler.github.io](https://einhungerkuenstler.github.io)

## Contents

- [Theme](#Theme)
  - [Maths](#Maths)
- [License](#license)

## Rationale

In March 2023, I had an idea to create my own personal webpage. Finally, after finishing my exams and during the summer vacation, I found the time to complete it. The main purpose of this webpage is to share some notes I've written on mathematics and physics. Additionally, I'll be sharing my interests in music, literature, philosophy, data science, quantitative finance and more. If I'm not feeling too lazy, I might also share some thoughts and experiences on this website!
##  Theme

I use the theme [catbook](https://github.com/starry99/catbook)
 
I have not changed any style of this theme, at least for now.

### Maths

  I decide to use Katex to render my maths. To get it to work, I just added the following html into my `head.html` file under my `_includes/` folder:

```html
<!-- Katex -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.16.8/dist/katex.min.css" integrity="sha384-GvrOXuhMATgEsSwCs4smul74iXGOixntILdUW9XmUC6+HX0sLNAK3q71HotJqlAn" crossorigin="anonymous">

<!-- The loading of KaTeX is deferred to speed up page rendering -->
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.8/dist/katex.min.js" integrity="sha384-cpW21h6RZv/phavutF+AuVYrr+dA8xD9zs6FwLpaCct6O9ctzYFfFr4dgmgccOTx" crossorigin="anonymous"></script>

<!-- To automatically render math in text elements, include the auto-render extension: -->
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.8/dist/contrib/auto-render.min.js" integrity="sha384-+VBxd3r6XgURycqtZ117nYw44OOcIax56Z4dCRWbxyPt0Koah1uHoK0o4+/RRE05" crossorigin="anonymous"
    onload="renderMathInElement(document.body);"></script>
```
Remeber you just could $$ but $ could not work.

For example, $$\int_{-\infty}^\infty e^{-x^2} dx = \sqrt{\pi}$$
## license

[MIT License](https://opensource.org/licenses/MIT)
