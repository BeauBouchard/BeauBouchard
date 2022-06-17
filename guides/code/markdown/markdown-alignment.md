
<p><a href="/">home</a> / <a href="/guides">guides</a></p>
<div class="rainbow-retro"></div>

# How to Align Content in Markdown

You have to use an HTML tag, Once you use an HTML tag in Markdown, everything between the open and closing tag must be also in HTML. 

You can directly attach `align=""` to any `HTML` tag, or create `<div>` or `<p>` tags with align properties attached to them. 


## Simple Usage

### Alignment an Image

#### Center

<p align="center">
  <img  width="100" height="100" src="http://beau.sh/assets/media/images/logos/sage.png?raw=true" />
</p>

#### Code

```
<p align="center">
  <img  width="100" height="100" src="http://beau.sh/assets/media/images/logos/sage.png?raw=true" />
</p>
```

---

#### Left

<p align="left">
  <img width="100" height="100" src="http://beau.sh/assets/media/images/logos/sage.png?raw=true" />
</p>

<p class="spacers"> <br /></p>

#### Code

```
<p align="left">
  <img width="100" height="100" src="http://beau.sh/assets/media/images/logos/sage.png?raw=true" />
</p>
```
---

#### Right
<p align="right">
  <img width="100" height="100" src="http://beau.sh/assets/media/images/logos/sage.png?raw=true" />
</p>
 
<p class="spacers"> </p>

#### Code

```
<p align="right">
  <img width="100" height="100" src="http://beau.sh/assets/media/images/logos/sage.png?raw=true" />
</p>
```

---


### Align other content using Div Tags

<div align="center">
  <img width="100" height="100" src="http://beau.sh/assets/media/images/logos/sage.png?raw=true">
  <img width="100" height="100" src="http://beau.sh/assets/media/images/logos/sage.png?raw=true">
  <img width="100" height="100" src="http://beau.sh/assets/media/images/logos/sage.png?raw=true">
</div>
  
<p class="spacers"> <br /></p>

#### Code

```
<div align="center">
  <img width="100" height="100" src="http://beau.sh/assets/media/images/logos/sage.png?raw=true">
  <img width="100" height="100" src="http://beau.sh/assets/media/images/logos/sage.png?raw=true">
  <img width="100" height="100" src="http://beau.sh/assets/media/images/logos/sage.png?raw=true">
</div>
```
<p class="spacers"> <br /></p>

## Advanced Usage


### NOTE:

It is no longer recommended to directly attach `align=""` to `<img/>` tags 

Read here: <a href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLImageElement/align">MDN HTML Documentation on 'align' property.</a>
