# An Exhibition of a Hunger Artist

Here is the blog of WHY: [https://einhungerkuenstler.github.io](https://einhungerkuenstler.github.io)

## Contents

- [Theme and Style](#theme-and-style)
      - [Maths](#maths)

## Rationale

I start to have the idea to have a personal webpage since four mouths ago. After the final exam and during the summer vacation, I finally get the time to make my personal webpage. This main purpose of this webpage is to use to put some notes of mathematics and physics written by me. Besides, I also share some personal favour on music, literature, philosophy, and so on. I will also share some life or thoughts on this website(If I am not so lazy!).
##  theme-and-style

I use the theme [catbook](https://github.com/starry99/catbook)
 
I have not change any style of this theme, at least for now.

### maths
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
## License

[MIT License](https://opensource.org/licenses/MIT)
