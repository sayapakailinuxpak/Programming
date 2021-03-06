# Module 4: Layout and positioning

## 4.1 Introduction

### Welcome to Module 4

<video src="https://edx-video.net/W3CCSS0I2016-V005000_DTH.mp4" preload="none" loop="loop" controls="controls" style="margin-left: 2em;" muted="" poster="http://www.multipelife.com/wp-content/uploads/2016/08/video-converter-software.png" width="180">
  <track src="https://courses.edx.org/courses/course-v1:W3Cx+CSS.0x+3T2018/xblock/block-v1:W3Cx+CSS.0x+3T2018+type@video+block@a9612f0ade0e4846a6fce8679b0f0873/handler/transcript/download" kind="captions" srclang="en" label="English" default>
  Your browser does not support the HTML5 video element.
</video>


### In this module, you will learn

+ How to use padding and margin to position elements relative to each other and the window
+ How to use alignment to control how your content sits within its HTML element
+ How to use the float property to let multiple HTML elements share horizontal space
+ How to use relative positioning to design your page so that it maintains its layout regardless of screen size


### Meet the box model

<video src="https://edx-video.net/W3CCSS0I2016-V004900_DTH.mp4" preload="none" loop="loop" controls="controls" style="margin-left: 2em;" muted="" poster="http://www.multipelife.com/wp-content/uploads/2016/08/video-converter-software.png" width="180">
  <track src="https://courses.edx.org/courses/course-v1:W3Cx+CSS.0x+3T2018/xblock/block-v1:W3Cx+CSS.0x+3T2018+type@video+block@d7de8c9c374b442c8dca24cbb32d0766/handler/transcript/download" kind="captions" srclang="en" label="English" default>
  Your browser does not support the HTML5 video element.
</video>


### The Box Model

The Box Model is how Web browsers see individual HTML elements. Each element is comprised of 4 areas: the __element__, the __padding__, the __border__ and the __margin__.

We discussed how to adjust the white space of these areas in Module 2.5, but in this module we will be discussing these areas as a method to position elements on a page.

<div style="display:flex;justify-content:center;align-items:center;flex-flow:row wrap;">
  <div><a href="https://courses.edx.org/courses/course-v1:W3Cx+CSS.0x+3T2018/courseware/2fb0b177f7594d2aa29f0ffa9e3b8b0a/cc87ccb0d8f243f98b2f17c1955c0298/1?activate_block_id=block-v1%3AW3Cx%2BCSS.0x%2B3T2018%2Btype%40vertical%2Bblock%408347080b2233486082d5154ee2e14ad6">
    <img src="https://prod-edxapp.edx-cdn.org/assets/courseware/v1/e0c6338dd98e9176bf12088bb686892f/asset-v1:W3Cx+CSS.0x+3T2018+type@asset+block/4-1_box_model.PNG" style="margin: 0.1em;" alt="anatomy of the box model" title="anatomy of the box model" width="400">
  </a></div>
</div>


+ __element__ - This is always contained within a square, even if it is a text block with jagged edges or a transparent image that isn't rectangular. Web browsers will impose a rectangle around the smallest area the HTML element's content actually occupies. Until now we've allowed the Web browser to determine the size of the element based solely on the content, but later in this section we'll learn how to adjust this sizing.
+ __padding__ - This is the white space just outside the element's content. You can set each of the four sides independently, and you can set the value to 0. If you set the element's background color, that color will apply to the padding as well.
+ __border__ - This is the area just outside the padding. Most HTML element's border default width is 0 and thus invisible. You can set each of the four sides independently. You can set a color, a pattern, even an image. This is a great way to add horizontal or vertical lines to an element on your page.
+ __margin__ - This is the space surrounding an element, outside the border. Margins are the part of HTML elements that interact with one another. When two margins interact the larger of the two wins meaning the smaller margin "collapses", thus the actual space between two elements is the larger of the two, not the sum of the margins.

[Example HTML](src/4.1-Box.html)
[Example CSS](src/css/4.1-Box.css)

#### External resource:

Box model definition in the [W3C's CSS2.1 specification](https://www.w3.org/TR/CSS2/box.html)



## 4.2 The basics of layout

### The alignment property

One of the simplest ways to align content is to use the direct text-align property. This can help you set the alignment of text or inline content within the context of their containing HTML element.

#### text-align

[Documentation](https://www.w3.org/TR/CSS22/text.html#alignment-prop)

```css
h1 {
   text-align: center;
}
```

If you have used a text editor before, like Microsoft Word, you've probably used the different text-align properties: left (default for English), right, center and justify. Text-align in CSS works the same way. Left, center and right specify how the lines of text within the text block are arranged. Justify sets the left and right edges of the text flush with the container's edges, which stretches the white space between words so that the overall block fits in a perfect rectangle.

See below for examples of what each of these values will do to your text:

<div style="display:flex;justify-content:center;align-items:center;flex-flow:row wrap;">
  <div><a href="https://courses.edx.org/courses/course-v1:W3Cx+CSS.0x+3T2018/courseware/2fb0b177f7594d2aa29f0ffa9e3b8b0a/8677e13b3db74668975ed449d681277e/1?activate_block_id=block-v1%3AW3Cx%2BCSS.0x%2B3T2018%2Btype%40vertical%2Bblock%40830982357f6646b796b37c238897fb9e">
    <img src="https://prod-edxapp.edx-cdn.org/assets/courseware/v1/8fa61e99d7f19f1e10862952f41a5128/asset-v1:W3Cx+CSS.0x+3T2018+type@asset+block/4-2-3_text_align.PNG" style="margin: 0.1em;" alt="Example of each text-align value options" title="Example of each text-align value options" width="350">
  </a></div>
</div>


Note that this property can only apply to block elements like paragraphs, divs and headers.

#### line-height

[Documentation](https://www.w3.org/TR/CSS22/visudet.html#line-height)

```css
h1 {
   line-height: 1.2;
}
```

You may have noticed that the text-align property sets the content's alignment horizontally, but it leaves its vertical alignment unchanged. Text lives within a specified vertical space, in which the text is drawn by default in the middle of that vertical space. If you change the height of the containing HTML block, the text will remain at the top of the block. However, if you instead use the "line-height" property, then the block will grow and the text will vertically center within it.


... and the resulting output:

<div style="display:flex;justify-content:center;align-items:center;flex-flow:row wrap;">
  <div><a href="https://courses.edx.org/courses/course-v1:W3Cx+CSS.0x+3T2018/courseware/2fb0b177f7594d2aa29f0ffa9e3b8b0a/8677e13b3db74668975ed449d681277e/1?activate_block_id=block-v1%3AW3Cx%2BCSS.0x%2B3T2018%2Btype%40vertical%2Bblock%40830982357f6646b796b37c238897fb9e">
    <img src="https://prod-edxapp.edx-cdn.org/assets/courseware/v1/3de7c0b54bd64eeffcf209a9928a95f0/asset-v1:W3Cx+CSS.0x+3T2018+type@asset+block/4-2-3_alignment-1.PNG" style="margin: 0.1em;" alt="output from alignment example code" title="output from alignment example code" width="450">
  </a></div>
</div>


#### INTERNATIONAL CONSIDERATIONS

Please do not use text-align indiscriminately. If there's a possibility that your site will need to be translated into a language that uses the Arabic, Hebrew, or Thaana scripts (which read from right to left), it creates difficulties to have to change all the  right values to left and vice versa.

Most, but not yet all, major browsers support the values start and end. The start value aligns text with the side of the line where you start reading, whether that's on the left for English or the right for Urdu. They also make more sense for use with vertical text, such as for Japanese and Mongolian. Once these values are widely supported by browsers, they will often be a better choice than right and left, since there's no need to change the values for pages as the language changes.

Also, note that CSS will in the future provide better support for justification in languages where words are not separated by spaces, such as Chinese and Thai, or languages where words are separated by special marks, such as in Amharic. For more information about different approaches to justification, see this article.

Once you finish this course, look out for these and other international features of CSS as you explore its features further.


### Element width and height

Until now we've let the browser decide how big the element is, but you can actually adjust its width and height manually.

#### Width and height

Documentation: [the width property](https://www.w3.org/TR/CSS22/visudet.html#the-width-property) and [the height property](https://www.w3.org/TR/CSS22/visudet.html#the-height-property)

```css
p {
   width: 30%;
}
```

You can use pixel values for both width and height, but you'll most often want to use percentages to set these so that your elements grow and shrink as appropriate based on the screen size.

For example, if we set the width of a paragraph to $30\%$ as you resize the browser window, you'll see how that element dynamically resizes. That's because when you use percentages, the size is computed based on the element's "[containing block](https://www.w3.org/TR/CSS22/visuren.html#containing-block)", or the element that contains the one you're styling. If your element is just within the body tag, the width is computed based on the relationship with the screen width.

Things are a bit more complicated with using a percentage to set an element's height. This is because typically the body's height is not specified, so if you use a percentage the size won't adjust.


#### min-width, max-width, min-height, max-height

Documentation: [max and min width](https://www.w3.org/TR/CSS22/visudet.html#min-max-widths) and [max and min height](https://www.w3.org/TR/CSS22/visudet.html#min-max-heights)

Setting width and height with percentages will save you work because your design will automatically optimize for the user's screen size. However, some elements can't grow and shrink as dynamically as text can.

For example, images will get "pixelated" if you let them grow too large, and they can look really distorted. Thankfully, you can set max and min width and heights. This way, you can set a range for your image to grow and shrink where you know it will still look good.

```css
img {
   width: 100%;
   max-width: 1024px;
}
```

[Example HTML](src/4.2-WidthHeight.html)<br/>
[Example CSS](src/css/4.2-WisthHeight.css)

When you view the above example, the paragraphs will dynamically resize based on the size of your window. For example, here is what the code looks like in a wide window:

<div style="display:flex;justify-content:center;align-items:center;flex-flow:row wrap;">
  <div><a href="https://courses.edx.org/courses/course-v1:W3Cx+CSS.0x+3T2018/courseware/2fb0b177f7594d2aa29f0ffa9e3b8b0a/8677e13b3db74668975ed449d681277e/1?activate_block_id=block-v1%3AW3Cx%2BCSS.0x%2B3T2018%2Btype%40vertical%2Bblock%40830982357f6646b796b37c238897fb9e">
    <img src="https://prod-edxapp.edx-cdn.org/assets/courseware/v1/433e61cced8e11e11f1478eb37983e5d/asset-v1:W3Cx+CSS.0x+3T2018+type@asset+block/4-2-1_wide.PNG" style="margin: 0.1em;" alt="dynamic width and height wide example" title="dynamic width and height wide example" width="550">
  </a></div>
</div>


However, here is the exact same code viewed in a much narrower window:

<div style="display:flex;justify-content:center;align-items:center;flex-flow:row wrap;">
  <div><a href="https://courses.edx.org/courses/course-v1:W3Cx+CSS.0x+3T2018/courseware/2fb0b177f7594d2aa29f0ffa9e3b8b0a/8677e13b3db74668975ed449d681277e/1?activate_block_id=block-v1%3AW3Cx%2BCSS.0x%2B3T2018%2Btype%40vertical%2Bblock%40830982357f6646b796b37c238897fb9e">
    <img src="https://prod-edxapp.edx-cdn.org/assets/courseware/v1/3d9b1840bdbdfaee3fcb0e6576da916f/asset-v1:W3Cx+CSS.0x+3T2018+type@asset+block/4-2-1_narrow.PNG" style="margin: 0.1em;" alt="dynamic width and high output narrow example" title="dynamic width and high output narrow example" width="200">
  </a></div>
</div>


Here, you can see that the elements have resized accordingly, but have hit the limits of their min and max constraints. This is why using percentages for width and height are so important, it helps you write code that works for all screen sizes.


### Padding and margin

Whenever possible, it is ideal to position your elements by adjusting their padding and margins. Sometimes this isn't enough to get the element exactly where you'd like it to be, so we'll learn more tools later in this module. Regardless, you'll almost always want some padding and margin around your element so it's best to adjust these before progressing onto more complicated positioning methods.

Once you have set the width for your element, then you can set margins as a way to position your element relative to others. One of the most commonly used margin settings is "auto". That is because if you set an element's left and right margin to auto it will be dynamically centered within its containing block.

```css
div {
   width: 50%;
   margin-left: auto;
   margin-right: auto;
}
```

However, note that this only works for block HTML elements like paragraphs, divs and headers. If you want to use this to position an inline element, such as img or a, you will need to tell CSS to treat them as block elements by setting display: block;

```css
img {
   display: block;
   width: 200px;
   margin-left: auto;
   margin-right: auto;
}
```

[Example HTML](src/4.2-Positioning.html) <br/>
[Example CSS](src/css/4.2-Positioning.css)

Here is what the above code looks like in a wide window:

<div style="display:flex;justify-content:center;align-items:center;flex-flow:row wrap;">
  <div><a href="https://courses.edx.org/courses/course-v1:W3Cx+CSS.0x+3T2018/courseware/2fb0b177f7594d2aa29f0ffa9e3b8b0a/8677e13b3db74668975ed449d681277e/1?activate_block_id=block-v1%3AW3Cx%2BCSS.0x%2B3T2018%2Btype%40vertical%2Bblock%40830982357f6646b796b37c238897fb9e">
    <img src="https://prod-edxapp.edx-cdn.org/assets/courseware/v1/8e7ce50235a81f6e65d0fe91084838bf/asset-v1:W3Cx+CSS.0x+3T2018+type@asset+block/4-2-2_wide.PNG" style="margin: 0.1em;" alt="centered elements with margin wide example" title="centered elements with margin wide example" width="550">
  </a></div>
</div>


Now, if you resize the window, the elements remain centered no matter what. Here is the above code in a narrow window:

<div style="display:flex;justify-content:center;align-items:center;flex-flow:row wrap;">
  <div><a href="https://courses.edx.org/courses/course-v1:W3Cx+CSS.0x+3T2018/courseware/2fb0b177f7594d2aa29f0ffa9e3b8b0a/8677e13b3db74668975ed449d681277e/1?activate_block_id=block-v1%3AW3Cx%2BCSS.0x%2B3T2018%2Btype%40vertical%2Bblock%40830982357f6646b796b37c238897fb9e">
    <img src="https://prod-edxapp.edx-cdn.org/assets/courseware/v1/e4842b904e93366d4b42b22e46440847/asset-v1:W3Cx+CSS.0x+3T2018+type@asset+block/4-2-2_narrow.PNG" style="margin: 0.1em;" alt="dynamically centered elements narrow example" title="dynamically centered elements narrow example" width="150">
  </a></div>
</div>


__External resources:__

+ A W3C CSS tip: [CSS centering things](https://www.w3.org/Style/Examples/007/center), on different ways to center your content.
+ A "CSS Tricks" article on [What you should know about collapsing margins](https://css-tricks.com/what-you-should-know-about-collapsing-margins/)



### Activity - Practice with alignment

For this activity, you are going to practice some of the basic alignment properties you've learned in this unit.

Here is some HTML and CSS:

```html
<!DOCTYPE html> 
<!--It's a best practice to always declare DOCTYPE!-->
<html lang="en">
  <head>
    <title>Practice with Alignment</title>
    <meta charset="utf-8">
  </head>
  <body>
    <header>
      <h1>Welcome to my web page</h1>
      <p>
        This is the tagline to my homepage
      </p>
    </header>
    <section>
      <h2>This is the main body of my page</h2>
      <article id="leftP">
        <h3>Article title</h3>
        This is a buch of text that will be left aligned under the main title of the page, 
        but still within the main center section of the page.
      </article>
      <article id="rightP">
        <h3>Article title</h3>
        Here is some more text that will be right aligned under the first paragraph, but 
        still within the main center section of the page.
      </article>
    </section>
    <footer>
      thank you and please visit again soon!
    </footer>
  </body>
</html>
```

```css
body {
  font-family: Tahoma;
}

header {
  background-color: #EC576B;
  color: white;
  border-bottom: 5px #FEDC3D solid;
}

header h1 {
  border-bottom: 2px #FFFFFF solid;
}

header p {
  border-bottom: 2px #FFFFFF solid;
}

section {
  background-color: #FEDC3D;
}

h2 {
  border-bottom: 5px #000000 solid;
}

article {
  background-color: #FFFFFF;
}

#leftP {

}

#rightP {

}

h3 {

}

footer {
  background-color: #4EC5C1;
  border-top: 5px #FEDC3D solid;
  color: white;
}
```

As it is, the given HTML and CSS codes produce the following Web page:

<div style="display:flex;justify-content:center;align-items:center;flex-flow:row wrap;">
  <div><a href="https://courses.edx.org/courses/course-v1:W3Cx+CSS.0x+3T2018/courseware/2fb0b177f7594d2aa29f0ffa9e3b8b0a/8677e13b3db74668975ed449d681277e/1?activate_block_id=block-v1%3AW3Cx%2BCSS.0x%2B3T2018%2Btype%40vertical%2Bblock%40830982357f6646b796b37c238897fb9e">
    <img src="https://prod-edxapp.edx-cdn.org/assets/courseware/v1/ac176f1517ec268dcb30bb52998246a1/asset-v1:W3Cx+CSS.0x+3T2018+type@asset+block/4-2-4_before.PNG" style="margin: 0.1em;" alt="Practice with Alignment before image" title="Practice with Alignment before image" width="450">
  </a></div>
</div>


As you can see it's not very well aligned. Your goal is to add properties to the existing CSS rules so that the final page looks like this:

<div style="display:flex;justify-content:center;align-items:center;flex-flow:row wrap;">
  <div><a href="https://courses.edx.org/courses/course-v1:W3Cx+CSS.0x+3T2018/courseware/2fb0b177f7594d2aa29f0ffa9e3b8b0a/8677e13b3db74668975ed449d681277e/1?activate_block_id=block-v1%3AW3Cx%2BCSS.0x%2B3T2018%2Btype%40vertical%2Bblock%40830982357f6646b796b37c238897fb9e">
    <img src="https://prod-edxapp.edx-cdn.org/assets/courseware/v1/eaf30118ca2b8f2fe5fda30a25c2c3d2/asset-v1:W3Cx+CSS.0x+3T2018+type@asset+block/4-2-4_after.PNG" style="margin: 0.1em;" alt="Practice with alignment after picture" title="Practice with alignment after picture" width="450">
  </a></div>
</div>


To do this you will need to:

+ remove the margin at the very edges of the page so the header and footer touch the edges of the page.
+ limit the size of the h1 title to 50% of the page's width, with horizontally centered text and vertically centered text within a height of 75px.
+ stretch the height of the header p to 50px, but let the text remain top aligned
+ limit the width of the section to 75% of the page, but never less than 500px. The section should be centered within the window.
+ limit the width of the h2 to 30% of the section, centered within that container. It should have a padding of 30px all around it.
+ limit the width of each article to 40% of the width of the section, with justified text. Each should have a margin of 50px all around it, a top padding of 10px, a left and right padding of 15px and a bottom padding of 30px. The h3 within each article should be aligned to the right.
+ give the #leftP article a left margin of 10% of the section.
+ give the #rightP article a left margin of 50% of the section.
+ limit the footer height to 10% of the page, but no more than 50px and no less than 10px. It should have a padding of 10px and a margin between it and the section of 30px.

Use the discussion below to discuss your experiences.


## 4.3 Floating elements

### Meet the float property

<video src="https://edx-video.net/W3CCSS0I2016-V005400_DTH.mp4" preload="none" loop="loop" controls="controls" style="margin-left: 2em;" muted="" poster="http://www.multipelife.com/wp-content/uploads/2016/08/video-converter-software.png" width="180">
  <track src="https://courses.edx.org/courses/course-v1:W3Cx+CSS.0x+3T2018/xblock/block-v1:W3Cx+CSS.0x+3T2018+type@video+block@aac339b219e0474daddc7e7cfc627a34/handler/transcript/download" kind="captions" srclang="en" label="English" default>
  Your browser does not support the HTML5 video element.
</video>

### The float property

If your elements are still not exactly where you want them to be after adjusting the padding, margins and alignment, then you can try out the float property. The "float" property is one of the most powerful tools you can master when learning CSS.

[Documentation](https://www.w3.org/TR/CSS22/visuren.html#float-position)

```css
h1 {
   width: 20em;
   float: right;
}
```

Up until now, we haven't moved elements very far from wherever the web browser automatically places them, but as you've probably noticed this has left our page very left side heavy. This is because, by default, elements are stacked one on top of the other, and they don't share horizontal space. With the float property, we can change this.

The float property liberates an element from its automatic position and lifts it up to "float" on top of other elements in the direction you specify.  You can specify float either right, left or the default of none.

Elements underneath a floating object will automatically wrap themselves around the content. For example, if you float an image, the text underneath will wrap around it so that none of it is actually obscured underneath the image, but now both text and an image can share horizontal space.

<div style="display:flex;justify-content:center;align-items:center;flex-flow:row wrap;">
  <div><a href="https://courses.edx.org/courses/course-v1:W3Cx+CSS.0x+3T2018/courseware/2fb0b177f7594d2aa29f0ffa9e3b8b0a/78bb3347b1a747dcb8b73dd7ef309e50/1?activate_block_id=block-v1%3AW3Cx%2BCSS.0x%2B3T2018%2Btype%40vertical%2Bblock%40fc1f61466cbb45e191c5030fdd9bf38e">
    <img src="https://prod-edxapp.edx-cdn.org/assets/courseware/v1/c631ba121850e9a7653d7b877f7ef05b/asset-v1:W3Cx+CSS.0x+3T2018+type@asset+block/4-3_float_img.PNG" style="margin: 0.1em;" alt="example of floating img and surrounding text" title="example of floating img and surrounding text" width="350">
  </a></div>
</div>


You'll often want to set the width of a floating object so that you have tighter control over the space that object occupies. Remember that, by default, block HTML elements occupy the entire width of the page, even if there isn't actual content that extends that far. In this case, you'll want to set the width so that your element's size more accurately represents its content and you don't have unnecessary white space. 


### The Clear Property

Once you have some elements floating things can get a little messy. It's easy for floating objects to overlap, and to prevent this you can use the "clear" property.

[Documentation](https://www.w3.org/TR/CSS22/visuren.html#propdef-clear)

```css
p {
   clear: both;
}
```

HTML code:

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8">
    </head>
  <body>
   <div id="default">
   This div is not floating, has no width set. (Red)
   </div>
   <div id="floatRightNoWidth">
   This div is floating right, but no width is set. (orange)
   </div>
   <div id="floatRightTooWide">
   This div is floating right, but the text is very very very long. This makes the div 
   fill the horizontal space of the page by default, so when it is floated it doesn't 
   look like it goes anywhere. (Yellow)
   </div>
   <div id="noFloatWidthSet">
   This div isn't floating, and its width is set to 40%. Floating elements can overlap. (Green)
   </div>
 
   <div id="floatRightWidthSet">
   This div is floating right, and its width is set to 30% (blue)
   </div>
   <div id="noFloatClearRight">
   This div isn't floating, and it is set to clear to the right, so nothing can overlap. (Purple)
   </div>
  </body>
</html>
```

CSS code:

```css
body {
   font-size: 24pt;
   font-family: helvetica, sans-serif;
}
div {
   margin-bottom: 10px;
}
#default {
   background-color: red;
}
#floatRightNoWidth {
   background-color: orange;
   float: right;
}
#floatRightTooWide {
   background-color: yellow;
   float: right;
}
#noFloatWidthSet {
   background-color: green;
   width: 40%;
}
#noFloatClearRight {
   background-color: purple;
   clear: right;
}
#floatRightWidthSet {
   background-color: blue;
   width: 30%;
   float: right;
}
```

... and the resulted output image:

<div style="display:flex;justify-content:center;align-items:center;flex-flow:row wrap;">
  <div><a href="https://courses.edx.org/courses/course-v1:W3Cx+CSS.0x+3T2018/courseware/2fb0b177f7594d2aa29f0ffa9e3b8b0a/78bb3347b1a747dcb8b73dd7ef309e50/1?activate_block_id=block-v1%3AW3Cx%2BCSS.0x%2B3T2018%2Btype%40vertical%2Bblock%40fc1f61466cbb45e191c5030fdd9bf38e">
    <img src="https://prod-edxapp.edx-cdn.org/assets/courseware/v1/445a62ab3ed7255b919c73ceac322320/asset-v1:W3Cx+CSS.0x+3T2018+type@asset+block/4-3_float.PNG" style="margin: 0.1em;" alt="Result of float example code" title="Result of float example code" width="350">
  </a></div>
</div>


### Activity - Practice with float

One of the toughest parts of layouts with CSS is figuring out which elements to apply a float property to.

Here is [some HTML and CSS](https://codepen.io/techie4good/pen/xEbWrp):


HTML code:

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8">
        <title>My HTML page</title>
        <link rel="stylesheet" href="style.css">
    </head>
  <body>
   <header>
    <h2>welcome greeting subtitle</h2>
    <h1>Homepage Title</h1>
   </header>
  <section id="navigation">
   <ul>
    <li>nav link 1</li>
    <li>nav link 2</li>
    <li>nav link 3</li>
    <li>nav link 4</li>
    </ul>
   </section>
   <section id="content">
    <div id="topRight">
    If your elements are still not exactly where you want them to be after adjusting 
    the padding, margins and alignment, then you can try out the float property. 
    The "float" property is one of the most powerful tools you can master when learning CSS.
    </div>
    <div id="topLeft">
    Up until now, we haven't moved elements very far from wherever the web browser automatically 
    places them, but as you've probably noticed this has left our page very left side heavy.
    </div>
    <div id="bottomRight">
    The float property liberates an element from its automatic position and lifts it up to "float" 
    on top of other elements in the direction you specify.  You can specify float either right, 
    left or the default of none.
    </div>
    <div id="bottomLeft">
    Elements underneath a floating object will automatically wrap themselves around the content. 
    For example, if you float an image, the text underneath will wrap around it so that none 
    of it is actually obscured underneath the image.
    </div>
   </section>
  </body>
</html>
```

CSS code:

```css
body {
   background-color: #4ABDAC;
   color: #FFFFFF;
   font-family: Georgia, serif;
}
header {
   background-color: #F7B733;
   height: 75px;
}
 
h1 {
   padding: 15px;
}
#navigation {
   height: 30px;
   width: 30%;
   margin-left: auto;
   margin-right: auto;
}
 
#navigation li:hover {
   border-bottom: 1px #FC4A1A solid;
}
#content {
   background-color: #DFDCE3;
   width: 50%;
   margin: 0 auto;
}
div {
   background-color: #FC4A1A;
   width: 250px;
   height: 150px;
   padding: 10px;
   margin: 20px;
}
```

As you can see the layout is pretty messy. Your job in this activity is to decide which elements deserve a float property. You might also need to adjust some widths, margins and paddings to get everything looking like the final image below:

<div style="display:flex;justify-content:center;align-items:center;flex-flow:row wrap;">
  <div><a href="https://courses.edx.org/courses/course-v1:W3Cx+CSS.0x+3T2018/courseware/2fb0b177f7594d2aa29f0ffa9e3b8b0a/78bb3347b1a747dcb8b73dd7ef309e50/1?activate_block_id=block-v1%3AW3Cx%2BCSS.0x%2B3T2018%2Btype%40vertical%2Bblock%40fc1f61466cbb45e191c5030fdd9bf38e">
    <img src="https://prod-edxapp.edx-cdn.org/assets/courseware/v1/8fa8e85bccbafdea433ff8666300430e/asset-v1:W3Cx+CSS.0x+3T2018+type@asset+block/4-3-2_activity_output.PNG" style="margin: 0.1em;" alt="Practice with Float final result" title="Practice with Float final result" width="450">
  </a></div>
</div>


__HINT__: Pay close attention to the IDs applied to the HTML elements



## 4.4 Relative positioning

### Meet relative positioning

<video src="https://edx-video.net/W3CCSS0I2016-V005300_DTH.mp4" preload="none" loop="loop" controls="controls" style="margin-left: 2em;" muted="" poster="http://www.multipelife.com/wp-content/uploads/2016/08/video-converter-software.png" width="180">
  <track src="https://courses.edx.org/courses/course-v1:W3Cx+CSS.0x+3T2018/xblock/block-v1:W3Cx+CSS.0x+3T2018+type@video+block@5f16c9019b6b4e0ab7ba5b7b0ec29532/handler/transcript/download" kind="captions" srclang="en" label="English" default>
  Your browser does not support the HTML5 video element.
</video>


### The position property

The "position" property sets the algorithm for how the Web browser will compute the way the HTML elements are placed on the page. There are four different value options for the position property: 

+ __relative__ - This is the position setting we will be discussing in detail as it is the best way to build on the dynamic layout methods we have learned thus far. This lets you specify where an HTML element should be relative to where it would be by default.
+ __static__ - This is the default setting and will place an element wherever the web browser computes it should be.
+ __fixed__ - This places an element in a specific location within the window. You can use this to set an element to remain where it is regardless of scrolling. This was used heavily when "frames" were popular, however now it should be used very sparingly.
+ __absolute__ - This allows you to position elements relative to their containing box. This removes an element from its normal flow (just like a floating element) so it can be difficult to control and make a layout that is truly dynamic.

[Documentation](https://www.w3.org/TR/CSS22/visuren.html#choose-position)

```css
div {
   position: relative;
}
```

Once you've set the position to "relative" that frees you up to set the top, right, bottom and left properties- otherwise known as the "box offsets". These properties specify the distance between this object and its normal static position and the corner of the box that we are specifying.

For example, if we set the "left" to be "30px", it will move the element 30px to the right away from the left of where it was placed by default.

```css
p {
   position: relative;
   left: 30px;
}
```

[Documentation](https://www.w3.org/TR/CSS22/visuren.html#position-props)

Note that position is not an inherited property so you will have to apply it individually to each element. Because of this it is best to use this approach to designing your layout sparingly and should only be used after you cannot achieve your desired layout with alignment or floating. 


First example with this CSS code:

```css
h1 {
   background-color: red;
   width: 300px;
   position: relative;
   left: 150px;
}
section {
   background-color: orange;
   height: 100px;
}
h2 {
   position: relative;
   top: 20px;
}
footer {
   background-color: yellow;
   height: 200px;
   width: 300px;
   position: relative;
   left: 50px;
   top: 50px;
}
h3 {
   position: relative;
   top: 50px;
   left: 10px;
}
```

.... gives this output:

<div style="display:flex;justify-content:center;align-items:center;flex-flow:row wrap;">
  <div><a href="https://courses.edx.org/courses/course-v1:W3Cx+CSS.0x+3T2018/courseware/2fb0b177f7594d2aa29f0ffa9e3b8b0a/14550b18e08e46ed8b8f19621768cab4/1?activate_block_id=block-v1%3AW3Cx%2BCSS.0x%2B3T2018%2Btype%40vertical%2Bblock%400e765880600543b3ab4add58441fbb59">
    <img src="https://prod-edxapp.edx-cdn.org/assets/courseware/v1/a4ce8d619c1e91db563362743d829e21/asset-v1:W3Cx+CSS.0x+3T2018+type@asset+block/css-intro-4-4-position1.png" style="margin: 0.1em;" alt="Relative positioning - no overlap" title="Relative positioning - no overlap" width="350">
  </a></div>
</div>


Note that relative positioning can make elements overlap - check the following CSS code as a second example:

```css
h1 {
   background-color: red;
   width: 300px;
   position: relative;
   left: 150px;
}
section {
   background-color: orange;
   height: 100px;
}
h2 {
   position: relative;
   top: 20px;
}
footer {
   background-color: yellow;
   height: 200px;
   width: 300px;
   position: relative;
   left: 50px;
   top: -50px;
}
h3 {
   position: relative;
   top: 50px;
   left: 10px;
}
```

... that gives this different output:

<div style="display:flex;justify-content:center;align-items:center;flex-flow:row wrap;">
  <div><a href="https://courses.edx.org/courses/course-v1:W3Cx+CSS.0x+3T2018/courseware/2fb0b177f7594d2aa29f0ffa9e3b8b0a/14550b18e08e46ed8b8f19621768cab4/1?activate_block_id=block-v1%3AW3Cx%2BCSS.0x%2B3T2018%2Btype%40vertical%2Bblock%400e765880600543b3ab4add58441fbb59">
    <img src="https://prod-edxapp.edx-cdn.org/assets/courseware/v1/fecd6b132ba6083f0694307af1dc85c0/asset-v1:W3Cx+CSS.0x+3T2018+type@asset+block/css-intro-4-4-position2.png" style="margin: 0.1em;" alt="Relative positioning - overlap" title="Relative positioning - overlap" width="350">
  </a></div>
</div>


### Activity - Practice with relative positioning

For this activity, we are going to focus on using relative positioning to adjust how items sit on the page.

Here is some [HTML and CSS](https://codepen.io/techie4good/pen/KgwRwg)

Your task is to add CSS so that you achieve this final layout:

<div style="display:flex;justify-content:center;align-items:center;flex-flow:row wrap;">
  <div><a href="https://courses.edx.org/courses/course-v1:W3Cx+CSS.0x+3T2018/courseware/2fb0b177f7594d2aa29f0ffa9e3b8b0a/14550b18e08e46ed8b8f19621768cab4/1?activate_block_id=block-v1%3AW3Cx%2BCSS.0x%2B3T2018%2Btype%40vertical%2Bblock%400e765880600543b3ab4add58441fbb59">
    <img src="https://prod-edxapp.edx-cdn.org/assets/courseware/v1/96e4824c9970225df71220b783177964/asset-v1:W3Cx+CSS.0x+3T2018+type@asset+block/4-4_activity_output.PNG" style="margin: 0.1em;" alt="Relative positioning activity output" title="Relative positioning activity output" width="450">
  </a></div>
</div>


You can do this with padding and margins, but limit yourself to only add position, top and left properties. Try resizing your browser window, and if you've implemented everything correctly all the elements will stay in the same position relative to one another.


## 4.5 Style studies

### Menus

One of the most important aspects of any Web site is the navigation menu. Over time, top level navigation has become fairly standardized so your user will be looking for some key elements that help them find their way around your site:

A small group of descriptive links in a rectangular arrangement, often horizontally
A hover style to give your user some amount of responsiveness
A special style indicating the link for the page you are currently on

#### Menu 1

This is a very basic menu design. It floats the list elements to the left and gives them each a simple hover property (underline) and a new background color for the link representing the page you are currently viewing.

<div style="display:flex;justify-content:center;align-items:center;flex-flow:row wrap;">
  <div><a href="https://courses.edx.org/courses/course-v1:W3Cx+CSS.0x+3T2018/courseware/2fb0b177f7594d2aa29f0ffa9e3b8b0a/715961f4bb784c38a01f469bb345ee7b/1?activate_block_id=block-v1%3AW3Cx%2BCSS.0x%2B3T2018%2Btype%40vertical%2Bblock%404c834437628a4b35844d8d2e10d8dedf">
    <img src="https://prod-edxapp.edx-cdn.org/assets/courseware/v1/6985026ba90be845a330a399bc6b59a1/asset-v1:W3Cx+CSS.0x+3T2018+type@asset+block/4-5_menu_1.PNG" style="margin: 0.1em;" alt="Menu 1 design" title="Menu 1 design" width="450">
  </a></div>
</div>


#### Menu 2

This menu design uses a vertical arrangement but still floats the overall menu object so it can sit level with your content. You can also see a tabbed format here where the page you are currently viewing directly connects to the menu item representing it. 

<div style="display:flex;justify-content:center;align-items:center;flex-flow:row wrap;">
  <div><a href="https://courses.edx.org/courses/course-v1:W3Cx+CSS.0x+3T2018/courseware/2fb0b177f7594d2aa29f0ffa9e3b8b0a/715961f4bb784c38a01f469bb345ee7b/1?activate_block_id=block-v1%3AW3Cx%2BCSS.0x%2B3T2018%2Btype%40vertical%2Bblock%404c834437628a4b35844d8d2e10d8dedf">
    <img src="https://prod-edxapp.edx-cdn.org/assets/courseware/v1/33113a2129d524c729491baf42660eab/asset-v1:W3Cx+CSS.0x+3T2018+type@asset+block/4-5_menu_2.PNG" style="margin: 0.1em;" alt="Menu 2 design" title="Menu 2 design" width="450">
  </a></div>
</div>


#### Menu 3

This third design employs hover as a way to expose secondary links. This lets you leave the top level clean and simple but gives the user the power of more specific options when they interact with your header.

<div style="display:flex;justify-content:center;align-items:center;flex-flow:row wrap;">
  <div><a href="https://courses.edx.org/courses/course-v1:W3Cx+CSS.0x+3T2018/courseware/2fb0b177f7594d2aa29f0ffa9e3b8b0a/715961f4bb784c38a01f469bb345ee7b/1?activate_block_id=block-v1%3AW3Cx%2BCSS.0x%2B3T2018%2Btype%40vertical%2Bblock%404c834437628a4b35844d8d2e10d8dedf">
    <img src="https://prod-edxapp.edx-cdn.org/assets/courseware/v1/e082cebfa12f01a129b47d94dd0a929a/asset-v1:W3Cx+CSS.0x+3T2018+type@asset+block/4-5_menu_3.PNG" style="margin: 0.1em;" alt="menu 3 design" title="menu 3 design" width="450">
  </a></div>
</div>


### Footers

The footer of your page is typically the last thing your user will see, so it's important that you provide them any essential information. Typically, you will see footers that just contain contact info, but often they can also include navigation links, search bars or other calls to action.

You will want your footer to flow with your overall page design, but to be distinct from your content.

#### Footer 1

This is a basic footer that uses background color to help it stand out from the rest of the content. It contains contact links and a subtle reference to the designer of the page.

<div style="display:flex;justify-content:center;align-items:center;flex-flow:row wrap;">
  <div><a href="https://courses.edx.org/courses/course-v1:W3Cx+CSS.0x+3T2018/courseware/2fb0b177f7594d2aa29f0ffa9e3b8b0a/715961f4bb784c38a01f469bb345ee7b/1?activate_block_id=block-v1%3AW3Cx%2BCSS.0x%2B3T2018%2Btype%40vertical%2Bblock%404c834437628a4b35844d8d2e10d8dedf">
    <img src="https://prod-edxapp.edx-cdn.org/assets/courseware/v1/9c135af0d1fef9c55f3107993e8b7e88/asset-v1:W3Cx+CSS.0x+3T2018+type@asset+block/4-5_footer_1.PNG" style="margin: 0.1em;" alt="footer 1 design" title="footer 1 design" width="450">
  </a></div>
</div>


#### Footer 2

This footer provides navigation links. Because the footer is at the bottom of the page, you can get away with more links being exposed because limiting area isn't as important as in the top level header.

<div style="display:flex;justify-content:center;align-items:center;flex-flow:row wrap;">
  <div><a href="https://courses.edx.org/courses/course-v1:W3Cx+CSS.0x+3T2018/courseware/2fb0b177f7594d2aa29f0ffa9e3b8b0a/715961f4bb784c38a01f469bb345ee7b/1?activate_block_id=block-v1%3AW3Cx%2BCSS.0x%2B3T2018%2Btype%40vertical%2Bblock%404c834437628a4b35844d8d2e10d8dedf">
    <img src="https://prod-edxapp.edx-cdn.org/assets/courseware/v1/9faaec50681a88db6ebed64764a8bee2/asset-v1:W3Cx+CSS.0x+3T2018+type@asset+block/4-5_footer_2.PNG" style="margin: 0.1em;" alt="Footer 2 design" title="Footer 2 design" width="450">
  </a></div>
</div>


#### Footer 3

This final design flows with the overall structure of the page, but limits the content to a single simple contact link.

<div style="display:flex;justify-content:center;align-items:center;flex-flow:row wrap;">
  <div><a href="https://courses.edx.org/courses/course-v1:W3Cx+CSS.0x+3T2018/courseware/2fb0b177f7594d2aa29f0ffa9e3b8b0a/715961f4bb784c38a01f469bb345ee7b/1?activate_block_id=block-v1%3AW3Cx%2BCSS.0x%2B3T2018%2Btype%40vertical%2Bblock%404c834437628a4b35844d8d2e10d8dedf">
    <img src="https://prod-edxapp.edx-cdn.org/assets/courseware/v1/015bf0799a0d0d1174f6f8817cf511af/asset-v1:W3Cx+CSS.0x+3T2018+type@asset+block/4-5_footer_3.PNG" style="margin: 0.1em;" alt="Footer design 3" title="Footer design 3" width="450">
  </a></div>
</div>



## 4.6 Project 4 - My resume

### When to use what?

Now that we are at the end of Module 4, you have a long list of different ways to move HTML elements around your page using CSS. With so many tools come choices, as you can now accomplish the same task multiple ways. Here are some guidelines on how to decide when to use which tool, in the order in which you should use them when positioning an element.

1) Use padding and margin whenever you can. This will keep things simple in relation to the box model and the overall flow of elements in relation to one another.
2) The float property is necessary when you want two block elements to share horizontal space. It can be easy to overuse the float property, keep in mind that if elements aren't floating the way you want them to you might want to adjust their order in the HTML instead of applying float to more and more elements.
3) If the above tools aren't getting your element where it should be, you can use relative positioning and directly set the box offsets (top, bottom, left, right). This makes things a bit more complicated especially when you try to inspect the box model around your element, but sometimes this is unavoidable because of collapsing margins. 
4) If all that is not enough, there are advanced CSS features such as flexbox, table layout, absolute positioning and grid layout. These will be taught in an advanced CSS course.



### Module 4 project - My resume

In Modules 2 and 3, you've been building on a Web page that displays personal information about you. For this module project, we are going to continue to build on that work and turn our profile into a "resume" or "CV". It's almost a requirement these days that you have a professional online presence, so this is a good way to start building that online portfolio.

Traditional printed resumes typically are required to fit on a single piece of paper (A4 or Letter sizes), which means they need to make very effective use of the space available. For this project, you are going to try to reproduce a typical resume layout but with HTML and CSS.

Here is what my Web resume looks like:

<div style="display:flex;justify-content:center;align-items:center;flex-flow:row wrap;">
  <div><a href="https://courses.edx.org/courses/course-v1:W3Cx+CSS.0x+3T2018/courseware/2fb0b177f7594d2aa29f0ffa9e3b8b0a/5999eaf51b77404eb43cdf0e62531fad/1?activate_block_id=block-v1%3AW3Cx%2BCSS.0x%2B3T2018%2Btype%40vertical%2Bblock%400e4ed413a4ba419ba83de5eda7ae06d2">
    <img src="https://prod-edxapp.edx-cdn.org/assets/courseware/v1/07fb2ab374e9dcd5a05257cf25507fde/asset-v1:W3Cx+CSS.0x+3T2018+type@asset+block/4-6_Kasey_Resume.PNG" style="margin: 0.1em;" alt="Kasey's web resume" title="Kasey's web resume" width="350">
  </a></div>
</div>

To more closely simulate a paper resume, your entire page's content must be centered in the middle 75% of the page. All your content should remain centered, and in the same position relative to the other elements on the page when you resize the browser window.

For this project you must at least:

+ Use percentages to set the width of 3 elements
+ Change the text-alignment property to something other than "left" on at least 1 element
+ Have 4 floating elements
+ Use the clear property once
+ Use the position property and box offsets to position at least 2 elements



## 4.7 Conclusion and exercises

### After Module 4, you should be able to...

+ Control exactly where an HTML element is placed on a page
+ Design the layout of your HTML elements such that they stay aligned as the window grows and shrinks
+ Employ the alignment, float and position properties when appropriate for optimal page structure

In the next module, we'll...
+ Learn about how to design your Web page to meet your user's needs
+ Review historical web design trends and what we can learn from them
+ Explore current Web design styles and learn how to best use them


### Exercises (1-5)

Use the following diagram representing the box model to answer questions 1, 2 and 

<div style="display:flex;justify-content:center;align-items:center;flex-flow:row wrap;">
  <div><a href="https://courses.edx.org/courses/course-v1:W3Cx+CSS.0x+3T2018/courseware/2fb0b177f7594d2aa29f0ffa9e3b8b0a/60880ee11cf3463bb80468dfb9f19d2b/1?activate_block_id=block-v1%3AW3Cx%2BCSS.0x%2B3T2018%2Btype%40vertical%2Bblock%4046c0b6a1f3b1405aa8ba43aecec465e5">
    <img src="https://prod-edxapp.edx-cdn.org/assets/courseware/v1/c9a8a2e2fc13dbf7c17b4d68132bf6f1/asset-v1:W3Cx+CSS.0x+3T2018+type@asset+block/4-7-1_box_model.PNG" style="margin: 0.1em;" alt="Box model showing regions a, b, c and d" title="Box model showing regions a, b, c and d" width="350">
  </a></div>
</div>


1. "Region C"

    What is the name of the region labeled "Region C" above?

    Ans: padding

2. "Region A"

    What is the name of the region labeled "Region A" above?

    Ans: margin


3. "Region B"

    What is the name of the region labeled "Region B" above?

    Ans: border


Use the following code to answer questions 4 and 5
HTML code:

```html
<section>
   <article>
      <h1>Header 1</h1>
   </article>
</section>
```

CSS code:

```css
section {
   width: 1000px;
}
article {
   width: 50%;
}
h1 {
   width: 10%;
}
```

4. Wide element

    Based on the HTML and CSS give, how wide will the article element be?
    1) 500px
    2) 50px
    3) 250px
    4) 100px
    5) 1000px

    Ans: 1 <br/>
    Explanation: 50% of 1000px equals 500px!


5. Wide h1

    Based on the HTML and CSS give, how wide will the h1 elements be?
    1) 500px
    2) 50px
    3) 250px
    4) 100px
    5) 1000px

    Ans: 2 <br/>
    Explanation: 10% of 50% of 1000px equals 50px ;)


### Exercises (6-10)

6. Avoiding pixelisation

    When displaying an image, what is the best way to integrate it into your design and prevent it from becoming too pixelated?

    1) Set your image's width to a percentage, and set its max-width so it cannot overgrow its quality
    2) Set your image's width to a percentage to let it dynamically resize with your user's window
    3) Set your image's width to a specific pixel size so it will not resize
    4) Upload the image in the desired dimensions, and do not let it resize with your design

    Ans: 2 <br/>
    Explanation: Pixelisation occurs when images are stretched, but not when they are shrunk. The max-width avoids that the image stretches.


7. Centering things

    What is the best way to dynamically center a block element horizontally within its containing element?

    1) Set the outer block element's left and right margins to auto
    2) Set the outer block element's text-align property to center
    3) Set the inner block element's left and right margins to auto
    4) Set the inner block element's text-align property to center

    Ans: 3, x1 <br/>
    Explanation: The text-align property affects text within a block, but not the block as a whole. The auto margins have to be on the block that is to be centered.


8. Centering in a block

    What is the best way to center the inline content, like text and images, horizontally within a block element?
    1) Set the inner block element's line-height to the size of the outer block element
    2) Set the block element's text-align property to center
    3) Set the block element's left and right margins to auto
    4) Set the inline content's text-align property to center

    Ans: 2, x3 <br/>
    Explanation: Inline content is affected by the text-align property. The margins on the block do not influence the alignment of inline content.


9. Vertical centering

    What is the simplest way to vertically center a single line of text content within a block element?
    1) Set the block element's line-height to the same value as the height of the block
    2) Set the block element's left and right margins to auto
    3) Set the block element's text-align property to center

    Ans: 1 <br/>
    Explanation: Text is put in the middle of the vertical space given by the line-height property. Text-align only works in the horizontal direction and the margins of the block element do not affect the alignment of the text within the element.


Use the following code to answer question 10:
HTML code:

```html
<h1> Header 1 </h1>
<h2> Header 2 </h2>
```

CSS code:

```css
h1 {
   margin: 50px;
}
h2 {
   margin: 10px;
}
```

10. Margin size

    Based on the HTML and CSS above, what is the resulting margin separating the H1 and H2 elements?
    1) 20px
    2) 50px
    3) 80px
    4) 30px

    Ans: 2 <br/>
    Explanation: The vertical margin between two elements is the largest of the two elements' margins.



### Exercises (11-14)

Use the following code to answer question 11:

HTML code:

```html
<article>
    <img src="images/myPic.jpg" alt="A boy raises his hand in a classroom" /> 
    <p>This is the test I would like to surround my image. This text is sitting 
      to the right of my image, and the image is touching the left of the window. </p>
</article>
```

The result:


<div style="display:flex;justify-content:center;align-items:center;flex-flow:row wrap;">
  <div><a href="https://courses.edx.org/courses/course-v1:W3Cx+CSS.0x+3T2018/courseware/2fb0b177f7594d2aa29f0ffa9e3b8b0a/60880ee11cf3463bb80468dfb9f19d2b/1?activate_block_id=block-v1%3AW3Cx%2BCSS.0x%2B3T2018%2Btype%40vertical%2Bblock%4046c0b6a1f3b1405aa8ba43aecec465e5">
    <img src="https://prod-edxapp.edx-cdn.org/assets/courseware/v1/06eebde78ad82ec57f0883100f27eedf/asset-v1:W3Cx+CSS.0x+3T2018+type@asset+block/4-7-2_float.PNG" style="margin: 0.1em;" alt="A boy raises his hand in a classroom" title="A boy raises his hand in a classroom" width="250">
  </a></div>
</div>


11. Left and right

    Which of the following CSS rules applied to the above HTML will result in the given image where the img is positioned to the left of the text on its right?
    1) `p { float: left; }`
    2) `img { float: left; }`
    3) `p { float: right; }`
    4) `img { float: right; }`

    Ans: 2 <br/>
    Explanation
    + p { float: right; } and p { float: left; } would both put the text below the image, because the p element would be as wide as the article.
    + img { float: right; } would put the image on the right.
    + img { float: left; } is the correct answer.


Use the following code to answer questions 12 and 13:

HTML code:

```html
<ul>
   <li>Amsterdam</li>
   <li>Bangkok</li>
   <li>Cairo</li>
   <li>Dubai</li>
</ul>
```

12. Float left

    In what order will the items (words) be displayed if the following CSS rule was applied to the above HTML?

    ```css
    li { float: left; }
    ```

    1) Dubai Cairo Bangkok Amsterdam
    2) Amsterdam Bangkok Cairo Dubai
    3) Cairo Dubai Amsterdam Bangkok
    4) Bangkok Cairo Dubai Amsterdam

    Ans: 2 <br/>
    Explanation: { float: left; } moves elements to the left as far as possible, but not further than any earlier elements in the list.


13. Float right

    In what order will the items (words) be displayed if the following CSS rule was applied to the above HTML?

    ```css
    li { float: right; }
    ```

    1) Dubai Cairo Bangkok Amsterdam
    2) Bangkok Cairo Dubai Amsterdam
    3) Cairo Dubai Amsterdam Bangkok
    4) Amsterdam Bangkok Cairo Dubai

    Ans: 1 <br/>
    Explanation: { float: right; } moves elements to the right as far as possible, but not further than any earlier elements in the list.


14. Relative positioning definition

    Which of the following best describes "relative positioning"?
    1) An element can be positioned relative to where it would be placed by default.
    2) An element can be positioned relative to its parent element with the same setting.
    3) An element can be positioned relative to the window such that as you scroll the element will remain in the same place.

    Ans: 1 <br/>
    Explanation: To keep an element fixed in the window, use "fixed positioning". To position an element reative to its parents, use "absolute positioning".


