footer: [speaking.scottgruber.me](https://speaking.scottgruber.me) @ UC Tech Santa Barbara 2019

# [fit] Web Tools
![80%, inline](img/uc-tech-logo-2019@2x.png)

^ How do you build websites? 

---
# What is in your toolkit?

---
![100%, original](img/microsoft.png)

^ 20+ years building websites

---

![300%, original](img/drupal.png)
![100%, original](img/microsoft.png)

---

![25%, original](img/WordPress.png)
![280%, original](img/drupal.png)
![50%, original](img/microsoft.png)

---
![25%, original](img/WordPress.png)
![280%, original](img/drupal.png)
![60%, original](img/JAMstack.png)
![60%, original](img/microsoft.png)

---

![25%, original](img/WordPress.png)
![280%, original](img/drupal.png)
![50%, original](img/laravel.png)
![50%, original](img/JAMstack.png)
![50%, original](img/microsoft.png)

---

# [fit] What is the nature of the web?
^ what are the foundations. what doesn't change?

--- 
![inline](img/html.png)

---
![inline](img/html-css.png)

---
![inline](img/html-css-js.png)

--- 
# What's else?

---
# [fit] A11Y

^ accessible, performance, aesthetics

--- 

# [fit] UX

^ work for everyone, loads fast, looks good.

--- 

# [fit] Design Systems  

---

# [fit] HTML & CSS
Flexbox, multi-column layout and CSS Grid
Microformats and semantic markup

---
[.hide-footer]

![fit](img/screenshots-1.png)

---

```html

<nav class="ucla-c-topic-nav">
<ul>
	<li><a href="#climate-change">Climate Change</a></li>
	<li><a href="#energy">Energy</a></li>
	<li><a href="#policy-law-regulation">Policy, Law &amp; Regulation</a></li>
	<li><a href="#economics-corporate-sustainability">Economics &amp; Corporate Sustainability</a></li>
</ul>
</nav>
```
---
# [fit] Flexbox

---

```css

.ucla-c-topic-nav ul {
    display: flex;
    flex-direction: column;
    list-style: none;
}

@media screen and (min-width: 30em) {
  .ucla-c-topic-nav ul {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
  }
} 
```

---

[.hide-footer]

![fit](img/screenshots-1.png)

---


```html

<h2><a id="climate-change"></a>Climate Change</h2>

<div class="ucla-c-faculty-advisors">

<ul>	
  <li><a href="#">Alan Barreca</a></li>	
  <li><a href="#">Alex Hall</a></li>
  <li><a href="#">Peter Kareiva</a></li>
  <li><a href="#">Liz Koslov</a></li>
</ul>

</div>

```
---
# [fit] Multi-Column

---

```css

@media screen and (min-width: 30em) {
  .ucla-c-faculty-advisors > ul {
    column-count: 3;
    column-gap: 1em;
  }
}

@media screen and (min-width: 60em) {
  .ucla-c-faculty-advisors > ul {
    column-count: 5;
    column-gap: 1em;
  }
}

```

---

[.hide-footer]

![fit](img/screenshots-2.png)

---

# [fit] Microformats and HTML5
---

```html

<div class="ucla-c-people-grid">

<article class="h-card">
  <a class="u-url" href="#">
    <h2 class="fn p-name">Jane Kitty Doe</h2>
    <img class="u-photo" src="https://placekitten.com/300/400" alt="kitten photo" />
    <p class="p-job-title">Assistant Professor</p>
    <small class="p-org">Institute of the Environment and Sustainability</small>
  </a>
</article>

<article class="h-card">
    ...
</article>
</div>
```
---

```html

<div class="ucla-c-people-grid">

<article class="h-card">
  <a class="u-url" href="#">
    <figure>
      <img class="u-photo" src="https://placekitten.com/300/400" alt="kitten photo" />
      <figcaption>
        <h2 class="fn p-name">Kitty Doe</h2>
        <p class="p-job-title">Assistant Professor</p>
        <small class="p-org">Institute of the Environment and Sustainability</small>
      </figcaption>
    </figure>
  </a>
  </article>

</div>

```
---
#[fit]CSS Grid

---

[.hide-footer]
![fit](img/screenshots-3.png)

---
[.hide-footer]
![fit](img/faculty-3col.jpg)

---

[.hide-footer]
![fit](img/faculty-2col.jpg)

---
[.hide-footer]
![fit](img/faculty-1col.jpg)

---
#[fit]RWD
^ responsive by default with no media queries

---


```css

.ucla-c-people-grid {
  display: grid;
  grid-gap: 2vw;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  grid-template-rows: auto;
}

```

---

```css

/* fall back if no grid support */
.ucla-c-people-grid > article {
    display: inline-block;
    margin: 1em;
    vertical-align: top;
    width: 300px;
}

.ucla-c-people-grid > img {
    height: auto;
    width: 200px;
}

```
---

```css

@supports (display: grid) {

    .ucla-c-people-grid {
        display: grid;
        grid-gap: 2vw;
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        grid-template-rows: auto;
    }

    /* reset properties */
    .ucla-c-people-grid > article {
        margin: initial;
        width: initial;
    }
}

```
---

# [fit] What's next?
--- 

![80%, inline](img/uc-tech-logo-2019@2x.png)

#[fit] Art Direction for the Web.
Thank you. 

