
<p><a href="/">home</a> / <a href="/guides">guides</a></p>
<div class="rainbow-retro"></div>

# Add a Decorative Drop-Cap to your Text

Having experimented a bit with this, adjusting the `font-size` and `line-height` can be an issue.

## Dropcap First Paragraph Only


<div class="guide-dropcap-01">
  <p>paragraph 1</p>
  <p>paragraph 2</p>
  <p>paragraph 3</p>
</div>

### Code

```html

<div class="guide-dropcap-01">
  <p>paragraph 1</p>
  <p>paragraph 2</p>
  <p>paragraph 3</p>
</div>

```

```css
/** Dropcap Only The First Paragraph **/
p:first-of-type:first-letter {
  color: #B91646;
  float: left;
  font-weight: bold;
  font-size: 2em;
  line-height: 1.9em;
  padding-right: 0.5em;
  margin-top: -0.1em;
} 
```


## Dropcap All Paragraphs


<div class="guide-dropcap-02">
  <p>paragraph 1</p>
  <p>paragraph 2</p>
  <p>paragraph 3</p>
</div>

### Code

```html
<div class="guide-dropcap-02">
  <p>paragraph 1</p>
  <p>paragraph 2</p>
  <p>paragraph 3</p>
</div>

```

```css
/** Dropcap All Paragraphs **/
p:first-child:first-letter {
  color: #B91646;
  float: left;
  font-weight: bold;
  font-size: 2em;
  line-height: 1.9em;
  padding-right: 0.5em;
  margin-top: -0.1em;
}

```

## Class Specific Dropcap

<p>paragraph 1</p>
<p>paragraph 2</p>
<p class="dropme">paragraph 3</p>


### Code

```html
<p>paragraph 1</p>
<p>paragraph 2</p>
<p class="dropme">paragraph 3</p>

```

```css
/** Just this Class will receive a dropcap **/
.dropme:first-letter {
  color: #B91646;
  float: left;
  font-weight: bold;
  font-size: 2em;
  line-height: 1.9em;
  padding-right: 0.5em;
  margin-top: -0.1em;
}

```

<p class="spacers"> <br /></p>

## NOTES


`1em` equals the font size of the parent element. 

`1rem` equals the font size of the html element, so adjusting the HTML's font size scales other sizes from it.


 * [Values_and_units](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Values_and_units)


The `:first-child` CSS pseudo-class represents the first element among a group of sibling elements.

 * [:first-child](https://developer.mozilla.org/en-US/docs/Web/CSS/:first-child)

The `:first-of-type` CSS pseudo-class represents the first element of its type among a group of sibling elements.

 * [:first-of-type](https://developer.mozilla.org/en-US/docs/Web/CSS/:first-of-type)


The `::first-letter` CSS pseudo-element applies styles to the first letter of the first line of a block-level element, but only when not preceded by other content (such as images or inline tables).

 * [::first-letter](https://developer.mozilla.org/en-US/docs/Web/CSS/::first-letter)


<p class="spacers"> <br /></p>
<div align="center" >
  <p>
    <a href="https://beau.sh/guides/">⬅️ Back to Guides</a>
  </p>
</div>
