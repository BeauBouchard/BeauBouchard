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

<p>Render a circle and adding a shadow to it allows you to overlay two circles</p>

```css

```
<p class="spacers"> </p>

<div class="guide-5830-l05"></div>

<p>The drop shadow then renders a smaller circle behind of that one</p>

```css

```

<p class="spacers"> </p>

<div class="guide-5830-l06"></div>


<p class="spacers"> </p>

<p>then cut them in half by turning off overflow, and moving the object slightly down, so the bounding box of the object is off-center, only showing half of it. and . . . </p>

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

.rainbow-pride {
  width: 35vw;
  height: 17.5vw;
  overflow: hidden;
  background: transparent;
  rotate: 180deg;
}

.rainbow-pride:after {
  position: absolute;
  content: '';
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

