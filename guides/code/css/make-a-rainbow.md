<p><a href="/">home</a> / <a href="/guides">guides</a></p>
<div class="rainbow-retro"></div>

# How to Make a rainbow with just CSS and HTML


<p class="spacers"> </p>
<p class="spacers"> </p>
<div class="rainbow-container">
  <div class="guide-rainbow-top"></div>
</div>
<p class="spacers"> </p>

<p>In this document you will learn to make the above rainbow only using CSS. </p>

<p class="spacers"> </p>

## How To . . . 


<p>Think of CSS as the ability to place shapes on your blank HTML page. </p>


<p>A rainbow is arches, but how do you make an arch shape in CSS?</p>

<div align="center">
  <img src="/assets/media/images/guides/images/neatpartyoudont.jpg" />
</div>

<p>like most things in CSS you just make borders or backgrounds layered, and smoothed till it looks something like the shape you wanted. Lets get started.</p>

<p class="spacers"> </p>

### Step 1 - Make a box

Start by making a class `rainbow` and adding it to any old `HTML` element. Make the class have an `:after` with `content: ''`, which allows it to render that after element to the page on load.

Because we are going to do multiple boxes, layered, an easy way of doing this is to use `drop-shadow`.

#### HTML

```html
<div class="rainbow-container">
  <div class="rainbow"></div>
</div>
```

#### CSS

```css
.rainbow-container {
  width: 500px;
  height: 200px;
  margin: auto;
  padding: 0;
}

.rainbow {
  position: relative;
  left: 200px;
  width: 1vw;
  height: 2vh;
  background: transparent;
  box-shadow:
    0 0 0 1vw #E7484F, // 1vw width
    0 0 0 2vw #F68B1D, // 1vw width
}
```
<p class="spacers"> </p>
<p class="spacers"> </p>
<div class="rainbow-container-flow">
  <div class="guide-rainbow-01"></div>
</div>
<p class="spacers"> </p>
<p class="spacers"> </p>

<p>You should see a single box like above</p>

### Step 2 - Make those Boxes Circles

#### CSS

```css
.rainbow {
  position: relative;
  left: 200px;
  width: 1vw;
  height: 2vh;
  border-radius: 50%;
  background: transparent;
  box-shadow:
    0 0 0 1vw #E7484F, // 1vw width
    0 0 0 2vw #F68B1D, // 1vw width
}
```

<p class="spacers"> </p>
<p class="spacers"> </p>
<div class="rainbow-container-flow">
  <div class="guide-rainbow-02"></div>
</div>
<p class="spacers"> </p>
<p class="spacers"> </p>

### Step 3 - Make more circles

#### CSS

```css
.rainbow {
  position: relative;
  width: 1vw;
  height: 2vh;
  border-radius: 50%;
  background: transparent;
  box-shadow:
    0 0 0 1vw #E7484F, // 1vw width
    0 0 0 2vw #F68B1D, // 1vw width
    0 0 0 3vw #FCED00, // 1vw width
    0 0 0 4vw #009E4F, // 1vw width
    0 0 0 5vw #00AAC3, // 1vw width
    0 0 0 6vw #732982; // 1vw width
}
```

<p class="spacers"> </p>
<p class="spacers"> </p>
<div class="rainbow-container-flow">
  <div class="guide-rainbow-03"></div>
</div>
<p class="spacers"> </p>
<p class="spacers"> </p>

<p class="spacers"> </p>

### Step 4 - Cut those Circles in half

<p>then cut them in half by turning off overflow, and moving the object slightly down, so the bounding box of the object is off-center, only showing half of it. and . . . </p>


#### HTML

```html
<div class="rainbow-container">
  <div class="rainbow"></div>
</div>
```


#### CSS

```css
// Put this around the rainbow
.rainbow-container {
  width: 500px;
  height: 200px;
  margin: auto;
  padding: 0;
  overflow: hidden;
}

.rainbow {
  position: relative;
  top: 190px;
  left: 200px;
  width: 1vw;
  height: 2vh;
  border-radius: 50%;
  background: transparent;
  /** This shadow box adds 0.5vw and 1vw width strips **/
  box-shadow:
    0 0 0 1vw #E7484F, // 1vw width
    0 0 0 2vw #F68B1D, // 1vw width
    0 0 0 3vw #FCED00, // 1vw width
    0 0 0 4vw #009E4F, // 1vw width
    0 0 0 5vw #00AAC3, // 1vw width
    0 0 0 6vw #732982; // 1vw width
    
    $theme-pride-six:                     #;
$theme-pride-seven:                   #;
$theme-pride-eight:                   #;
$theme-pride-nine:                    #;
$theme-pride-ten:                     #;
$theme-pride-eleven:                  #;
}
```
<p>Voilà . . . AN ARCH</p>

<div class="rainbow-container">
  <div class="guide-rainbow-04"></div>
</div>


<p class="spacers"> </p>

### Full Rainbow Example

<div class="rainbow-container">
  <div class="guide-rainbow-pride"></div>
</div>


<p class="spacers"> </p>

### Full Rainbow Example Code

#### HTML 

```html
<div class="rainbow-container">
  <div class="rainbow-pride"></div>
</div>
```

#### SCSS

```scss
/** Happy Pride Month Rainbow Colors **/
$theme-pride-one:                     #FBF9F5;
$theme-pride-two:                     #FEAEC7;
$theme-pride-three:                   #75D7EF;
$theme-pride-four:                    #613A15;
$theme-pride-five:                    #101010;
$theme-pride-six:                     #E7484F;
$theme-pride-seven:                   #F68B1D;
$theme-pride-eight:                   #FCED00;
$theme-pride-nine:                    #009E4F;
$theme-pride-ten:                     #00AAC3;
$theme-pride-eleven:                  #732982;

// Put this around the rainbow
.rainbow-container {
  width: 500px;
  height: 200px;
  margin: auto;
  padding: 0;
  overflow: hidden;
}

.rainbow-pride {
  position: relative;
  top: 190px;
  left: 200px;
  width: 1vw;
  height: 2vh;
  background: transparent;
  border-radius: 50%;
  /** This shadow box adds 0.5vw and 1vw width strips **/
  box-shadow:
    0 0 0 0.5vw $theme-pride-one,   // 0.5vw width
    0 0 0 1vw   $theme-pride-two,   // 0.5vw width
    0 0 0 1.5vw $theme-pride-three, // 0.5vw width
    0 0 0 2vw   $theme-pride-four,  // 0.5vw width
    0 0 0 2.5vw $theme-pride-five,  // 1vw width
    0 0 0 3.5vw $theme-pride-six,   // 1vw width
    0 0 0 4.5vw $theme-pride-seven, // 1vw width
    0 0 0 5.5vw $theme-pride-eight, // 1vw width
    0 0 0 6.5vw $theme-pride-nine,  // 1vw width
    0 0 0 7.5vw $theme-pride-ten,   // 1vw width
    0 0 0 8.5vw $theme-pride-eleven;// 1vw width
}
```
<p class="spacers"> </p>

