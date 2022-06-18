<p><a href="/">home</a> / <a href="/guides">guides</a></p>
<div class="rainbow-retro"></div>

# How to Make a rainbow with just CSS and HTML


<div class="guide-5830-l01"></div>

<p>In this document you will learn to make the above rainbow only using CSS. </p>

<p class="spacers"> </p>

## How To . . . 


<p>Think of CSS as the ability to place shapes on your blank HTML page. </p>


<p>A rainbow is arches, but how do you make an arch shape in CSS?</p>

<div align="center">
  <img src="/assets/media/images/guides/images/neatpartyoudont.jpg" />
</div>

<p class="spacers"> </p>

### Step 1 - Make a box

Start by making a class `rainbow` and adding it to any old `HTML` element. Make the class have an `:after` with `content: ''`, which allows it to render that after element to the page on load.

Because we are going to do multiple borders, we are going to do `drop-shadow` to that `:after`.

#### HTML

```html
<div class="rainbow"></div>
```

#### CSS

```css
.rainbow {
  width: 35vw;
  height: 17.5vw;
  background: #E7484F;
}

.ranbow:after {
  position: absolute;
  content: '';
  box-shadow: 0 0 0 1vw #F68B1D;
}
```

<p class="spacers"> </p>


<div class="guide-5830-l01"></div>

<p>You should see a single box like above</p>

### Step 2 - Make those Boxes Circles

#### CSS

```css
.rainbow {
  width: 35vw;
  height: 17.5vw;
  background: #E7484F;
}

.ranbow:after {
  position: absolute;
  content: '';
  box-shadow: 0 0 0 1vw #F68B1D;
}
```

### Step 3 - Make more circles

#### CSS

```css
.rainbow {
  width: 35vw;
  height: 17.5vw;
  background: #E7484F;
}

.ranbow:after {
  position: absolute;
  content: '';
  box-shadow: 0 0 0 1vw #F68B1D;
}
```

<div class="guide-5830-l06"></div>


<p class="spacers"> </p>

### Step 4 - Cut those Circles in half

<p>then cut them in half by turning off overflow, and moving the object slightly down, so the bounding box of the object is off-center, only showing half of it. and . . . </p>

#### CSS

```css
.rainbow {
  width: 35vw;
  height: 17.5vw;
  background: #E7484F;
}

.ranbow:after {
  position: absolute;
  content: '';
  box-shadow: 0 0 0 1vw #F68B1D;
}
```

<p>Voilà . . . AN ARCH</p>

<div class="guide-5830-l07"></div>

<p class="spacers"> </p>

### Full Rainbow Example

<div class="guide-container-rainbow-pride">
  <div class="guide-rainbow-pride"></div>
</div>


<p class="spacers"> </p>

### Full Rainbow Example Code

```scss
/** Happy Pride Month Rainbow Colors **/
.guide-container-rainbow-pride {
  width: 500px;
  height: 200px;
  margin: auto;
  padding: 0;
  overflow: hidden;
}

.guide-rainbow-pride {
  position: relative;
  top: 242px;
  left: 200px;
  width: 1vw;
  height: 2vh;
  background: transparent;
  border-radius: 50%;
  box-shadow: 
    0 0 0 0.5vw #FBF9F5,
    0 0 0 1vw   #FEAEC7,
    0 0 0 1.5vw #75D7EF,
    0 0 0 2vw   #613A15,
    0 0 0 2.5vw #101010,
    0 0 0 3.5vw #E7484F,
    0 0 0 4.5vw #F68B1D,
    0 0 0 5.5vw #FCED00,
    0 0 0 6.5vw #009E4F,
    0 0 0 7.5vw #00AAC3,
    0 0 0 8.5vw #732982;
}
```
<p class="spacers"> </p>

