
<p><a href="/">home</a> / <a href="/guides">guides</a></p>
<div class="rainbow-retro"></div>

# How to Align Content in Markdown

You have to use an HTML tag, Once you use an HTML tag in Markdown, everything between the open and closing tag must be also in HTML. 

You can directly attach `align=""` to any `HTML` tag, or create `<div>` tags with align properties attached to them. 

## Simple Usage

### Alignment an Image

#### Center

<img align="center" width="100" height="100" src="http://beau.sh/assets/media/images/logos/sage.png?raw=true" /><br />

#### Code

```
<img align="center" width="100" height="100" src="http://beau.sh/assets/media/images/logos/sage.png?raw=true" />
```

---

#### Left

<img align="left" width="100" height="100" src="http://beau.sh/assets/media/images/logos/sage.png?raw=true" /><br />




#### Code

```
<img align="left" width="100" height="100" src="http://beau.sh/assets/media/images/logos/sage.png?raw=true" />
```
---

#### Right

<img align="right" width="100" height="100" src="http://beau.sh/assets/media/images/logos/sage.png?raw=true" /><br />



#### Code

```
<img align="right" width="100" height="100" src="http://beau.sh/assets/media/images/logos/sage.png?raw=true" />
```

---


### Align other content using Div Tags

<div align="center">
  <img width="100" height="100" src="http://beau.sh/assets/media/images/logos/sage.png?raw=true">
  <img width="100" height="100" src="http://beau.sh/assets/media/images/logos/sage.png?raw=true">
  <img width="100" height="100" src="http://beau.sh/assets/media/images/logos/sage.png?raw=true">
</div>
  

#### Code

```
<div align="center">
  <img width="100" height="100" src="http://beau.sh/assets/media/images/logos/sage.png?raw=true">
  <img width="100" height="100" src="http://beau.sh/assets/media/images/logos/sage.png?raw=true">
  <img width="100" height="100" src="http://beau.sh/assets/media/images/logos/sage.png?raw=true">
</div>
```
