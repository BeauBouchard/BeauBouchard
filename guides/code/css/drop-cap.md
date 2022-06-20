
<p><a href="/">home</a> / <a href="/guides">guides</a></p>
<div class="rainbow-retro"></div>

# Add a decorative 

Having experimented a bit with this, adjusting the `font-size` and `line-height` can be an issue. Scale the paragraph to be 



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

```css
/** Just this Class will receive a dropcap **/
.justme:first-letter {
  color: #B91646;
  float: left;
  font-weight: bold;
  font-size: 2em;
  line-height: 1.9em;
  padding-right: 0.5em;
  margin-top: -0.1em;
}

```


## NOTES


 * `1em` equals the font size of the parent element. 
 * `1rem` equals the font size of the html element, so adjusting the HTML's font size scales other sizes from it.
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
