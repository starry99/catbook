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

  I decide to use MathJax to render my maths. To get it to work, I just added the following html into my `head.html` file under my `_includes/` folder:

```html
<script type="text/x-mathjax-config"> MathJax.Hub.Config({ TeX: { equationNumbers: { autoNumber: "AMS" } } }); </script>
<script type="text/x-mathjax-config">
  MathJax.Hub.Config({
	tex2jax: {
	  inlineMath: [ ['$','$'], ["\\(","\\)"] ],
	  processEscapes: true
	}
  });
</script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
```
## license

[MIT License](https://opensource.org/licenses/MIT)
