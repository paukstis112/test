---
title: Optimisations
category: Praktinės užduotys
order: 7
requirements:
  build: Any
  plan: Free
  hosting: CloudCannon
---

CloudCannon optimises sites to load as fast as possible. CloudCannon minifies CSS with [clean-css](https://github.com/GoalSmashers/clean-css) and JavaScript with [Uglifier](https://github.com/lautis/uglifier). Externally hosted assets are not optimised.

> Filenames containing **-min** or **.min** are not minified, as the filename suggests they have been minified already.

Assets referenced in the HTML and CSS are served from a CDN. Text based assets (e.g. HTML, CSS, and JavaScript) are gzipped before being served.

Optimisations are on by default, to toggle optimisations for your site:

1. Go to the *Site Settings* / *Build* section
2. Toggle **Minify and serve assets from CDN**
3. Click **Update Build Details**

---

To turn off optimisations on individual elements, add the `.cms-no-rewrite` class to the element.

~~~html
<a href="/newsletters/january-summary.pdf" class="cms-no-rewrite">Download Latest Newsletter</a>
~~~

The reference on the element remains the same, pointing to the unoptimised version.
