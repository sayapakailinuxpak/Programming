# Module 2: Attributes, images and links


## 2.1 Introduction to Module 2

### Welcome to Module 2

<video src="https://edx-video.net/W3CHTM502016-V014600_DTH.mp4" preload="none" loop="loop" controls="controls" style="margin-left: 2em;" muted="" poster="http://www.multipelife.com/wp-content/uploads/2016/08/video-converter-software.png" width="180">
  <track src="https://courses.edx.org/courses/course-v1:W3Cx+HTML5.0x+1T2019/xblock/block-v1:W3Cx+HTML5.0x+1T2019+type@video+block@7f247e6d116540ba8b4c263a05631dea/handler/transcript/download" kind="captions" srclang="en" label="English" default>
  Your browser does not support the HTML5 video element.
</video><br/>


### Meaningful Web pages

Tags and elements are building blocks of HTML5. However, they can be made so much more exciting with attributes. Let's take a simple element like list. You know how to add one to your page but can you change the order of your list? Or change it to an alphabetically ordered list instead of a numerical list? Can you display your list in reverse order? Yes, you can do all this and more using attributes.

Apart from exploring attributes for elements, we will continue to add life to our Web page by adding images and hyperlinks and learning about how to use and place them properly in your Web page.

In this module, we will also look at creating meaningful Web pages. Imagine you are the Web page designer of an online magazine. You want to have a central article, some aside commentary, captions, a summary of your article, addresses and citations. You also want to provide more detailed information such as, 'This sentence is really important and you need to convey that to the reader'.

If we just use `<p>` tags and header tags, `<h1>` to `<h6>`, visually it might look like what you want, but only a human will be able to read and understand the page. To a browser, there is very little information except that there is text and headings in your page. How can a search engine know what is important? Does a visually impaired person have to listen to the entire page or can just jump to the article?

It is very important to style your Web pages for search engines to improve your SEO rankings and for visually impaired people who access your Web page using assistive technology like screen readers. Semantic markup enables all of this and more.  


### Module 2 - Content

2.1 __Introduction__: Check out this video explaining what you'll be learning about in Module 2 - and wrap your mind around the concept of "semantic markup".

2.2 __Attributes__: Here you will build on to what you have already learned about attributes.

2.3 __Semantic meaning__: Explaining the difference between 'semantic' and 'style'.

2.4 __Images__: Learn how, when, and where to best utilize images in your Web pages.

2.5 __Hyperlinks__: They are the connections that allow the world to jump from place to place on the Web. Explore the secrets of this powerful mechanism!

2.6 __Exercises__ - Module 2: Lets check what you've learned during Module 2.


## 2.2 Attributes

### Introduction to attributes

We learned a little bit about what attributes are in the previous module. Let's look into it in more depth, by using examples.

Here is an ordered list:

```html
<ol>
  <li>Lights</li>
  <li>Camera</li>
  <li>Action</li>
</ol>
```

Output:

<ol>
  <li>Lights</li>
  <li>Camera</li>
  <li>Action</li>
</ol>

If i want an ordered list to start with the number 5 instead of 1 (as it does by default), let's code like this:

```html
<ol start="5">
  <li>Lights</li>
  <li>Camera</li>
  <li>Action</li>
</ol>
```

Output:

<ol start="5">
  <li>Lights</li>
  <li>Camera</li>
  <li>Action</li>
</ol>

Here, using the `start` attribute, we made our list start with 5 instead of 1.

Like `start`, we have many useful attributes we will see in this section that can affect your element. Attributes are a significant part of HTML. Tags and attributes make up the language. 


#### Syntax

Attributes are used in tags to further define the tag:

+ It is used inside the opening tag it is applied to and should be added after a space from the tag name: `<ol start="5">`. The start attribute is used inside the `<ol>` tag. 
+ `start="5"`<br/>Attribute name, equal sign, opening quote, attribute value, closing quote
+ Attributes are a name-value pair:` start="5"`<br/>name: start>br>value: any positive integer
+ The only exception to the name-value pair is if the attribute is a 'boolean attribute'. These attributes have only two types of values - true or false. But instead of writing "true" or "false" for its value, you add the attribute name to indicate true and omit it to indicate false. An example is the 'reversed' attribute in an ordered list `<ol>`. Adding this attribute is an indication that the list order should be reversed (in descending order).

  ```html
  <ol reversed></ol>
  ```

+ A tag can have multiple attributes:
  ```html
  <ol start="5"></ol>
  <ol id="cinema" class="attribute-list" start="5"></ol>
  <ol start="5" class="attribute-list"></ol>
  ```


#### Example 1: the 'id' attribute

Imagine you have two paragraphs in your HTML page:

```html
<p>I am paragraph 1 and I want to be in red</p>
<p>I am paragraph 2 and I want to be in blue</p>
```

Your task is to make the text color of the first paragraph <span style="color: red;">red</span> and the other <span style="color: blue;">blue</span>. How do we do that? You add styling to your HTML document through CSS. CSS is a style sheet language where you add any presentation related information for your HTML document. You will learn about this in the next chapter. In this case, you will have to write code in your style sheet to inform that it needs to change the text colors respectively. 

But to identify each paragraph, we need to give them each a name first so we can instruct our style sheet to make X red and Y blue. This unique name we give each element is called an 'ID'. This is very similar to your school or corporate ID that is unique to you. No one else in your company will have the same ID as you. id is an attribute. It should be unique to the element because we know that two people having the same ID will just cause a lot of confusion. 

```html
<p id="para1">I am paragraph 1 and I want to be in red</p>
<p id="para2">I am paragraph 2 and I want to be in blue</p>
```

Here, we can style `para1` and `para2` separately using CSS. The id attribute helps us do this by letting us give each paragraph an ID.


#### Example 2: the 'class' attribute

A similar attribute is `class`. `class` like `id` is a very useful attribute and one you will be using very frequently. Let's assume you are an author of a book. You like poems and you want to include at least 20 of them in your new book. You add IDs for them: 'poem1', 'poem2', 'poem3'.

You want your poems to look different from your other text. Grey text color, italic and bold. Like this:

<p style="text-rendering: optimizeLegibility; margin-right: 0px; margin-left: 0px; padding: 0px 0px 0px 30px; border: 0px; outline: 0px; font-stretch: inherit; font-size: 16px; font-family: 'Open Sans', 'Helvetica Neue', Helvetica, Arial, sans-serif; vertical-align: baseline;"><span style="text-rendering: optimizeLegibility; margin: 0px; padding: 0px; border: 0px; outline: 0px; font-style: inherit; font-variant: inherit; font-weight: inherit; font-stretch: inherit; font-size: inherit; line-height: 1.4em; font-family: inherit; vertical-align: baseline; color: #808080;"><em style="text-rendering: optimizeLegibility; margin: 0px; padding: 0px; border: 0px; outline: 0px; font-variant: inherit; font-weight: inherit; font-stretch: inherit; font-size: inherit; line-height: 1.4em; font-family: inherit; vertical-align: baseline;"><strong style="text-rendering: optimizeLegibility; margin: 0px; padding: 0px; border: 0px; outline: 0px; font-style: inherit; font-variant: inherit; font-stretch: inherit; font-size: inherit; line-height: 1.4em; font-family: inherit; vertical-align: baseline;">To move, to breathe, to fly, to float,</strong></em></span><br style="text-rendering: optimizeLegibility; line-height: 24px; color: #111111; font-family: Verdana, Helvetica, Arial, sans-serif; font-size: 15px; background-color: #fef3ea;"><span style="text-rendering: optimizeLegibility; margin: 0px; padding: 0px; border: 0px; outline: 0px; font-style: inherit; font-variant: inherit; font-weight: inherit; font-stretch: inherit; font-size: inherit; line-height: 1.4em; font-family: inherit; vertical-align: baseline; color: #808080;"><em style="text-rendering: optimizeLegibility; margin: 0px; padding: 0px; border: 0px; outline: 0px; font-variant: inherit; font-weight: inherit; font-stretch: inherit; font-size: inherit; line-height: 1.4em; font-family: inherit; vertical-align: baseline;"><strong style="text-rendering: optimizeLegibility; margin: 0px; padding: 0px; border: 0px; outline: 0px; font-style: inherit; font-variant: inherit; font-stretch: inherit; font-size: inherit; line-height: 1.4em; font-family: inherit; vertical-align: baseline;">To gain all while you give,</strong></em></span><br style="text-rendering: optimizeLegibility; line-height: 24px; color: #111111; font-family: Verdana, Helvetica, Arial, sans-serif; font-size: 15px; background-color: #fef3ea;"><span style="text-rendering: optimizeLegibility; margin: 0px; padding: 0px; border: 0px; outline: 0px; font-style: inherit; font-variant: inherit; font-weight: inherit; font-stretch: inherit; font-size: inherit; line-height: 1.4em; font-family: inherit; vertical-align: baseline; color: #808080;"><em style="text-rendering: optimizeLegibility; margin: 0px; padding: 0px; border: 0px; outline: 0px; font-variant: inherit; font-weight: inherit; font-stretch: inherit; font-size: inherit; line-height: 1.4em; font-family: inherit; vertical-align: baseline;"><strong style="text-rendering: optimizeLegibility; margin: 0px; padding: 0px; border: 0px; outline: 0px; font-style: inherit; font-variant: inherit; font-stretch: inherit; font-size: inherit; line-height: 1.4em; font-family: inherit; vertical-align: baseline;">To roam the roads of lands remote,</strong></em></span><br style="text-rendering: optimizeLegibility; line-height: 24px; color: #111111; font-family: Verdana, Helvetica, Arial, sans-serif; font-size: 15px; background-color: #fef3ea;"><span style="text-rendering: optimizeLegibility; margin: 0px; padding: 0px; border: 0px; outline: 0px; font-style: inherit; font-variant: inherit; font-weight: inherit; font-stretch: inherit; font-size: inherit; line-height: 1.4em; font-family: inherit; vertical-align: baseline; color: #808080;"><em style="text-rendering: optimizeLegibility; margin: 0px; padding: 0px; border: 0px; outline: 0px; font-variant: inherit; font-weight: inherit; font-stretch: inherit; font-size: inherit; line-height: 1.4em; font-family: inherit; vertical-align: baseline;"><strong style="text-rendering: optimizeLegibility; margin: 0px; padding: 0px; border: 0px; outline: 0px; font-style: inherit; font-variant: inherit; font-stretch: inherit; font-size: inherit; line-height: 1.4em; font-family: inherit; vertical-align: baseline;">To travel is to live.</strong></em></span></p>

So all poems have the same requirements.

If you use id attribute, you can instruct the stylesheet to style each poem in a particular way. It will look something like (we will learn how to write proper styles in the next chapter, so for now we will just phrase it in English) -

<p style="padding-left: 30px;">'Make poem1's&nbsp;text color grey, italic and bold'<br> 'Make poem2's&nbsp;text color grey, italic and bold'<br>'Make poem3's&nbsp;text color grey, italic and bold'</p>

Can you imagine how repetitive your style sheet will look if you have to instruct it to do the same thing 20 times for different poem IDs? HTML makes it easier. We use the class attribute. Let's name this class of poems 'poetry'. 

<p id="poem1" class="poetry">To move, to breathe, to fly, to float...</p>
<p id="poem2" class="poetry">Roses are red, violets are blue...</p>
So now, all you have to do in your style sheet, is to instruct it to make all elements belonging to the 'poetry' class grey, italic and bold. 

#### Knowledge check 2.2.1

```html
<ol id="student-male" class="primary" start="10"></ol>
<ol start="10" class="primary" id="student-male"></ol>
```

True or False? Both tags will give the same output. The order in which the attributes are specified in the opening tag does not matter.

  Ans: True, xFalse<br/>
  Explication: As long as they are specified in the start tag, their order does not matter. Most are a name-value pair but for some like 'reversed' (boolean attribute), just their presence can affect the element.



### Global & non-global attributes

You have seen a few examples of attributes now: `start`, `id` and `class`. All HTML elements have attributes.

There are two kind of attributes:

+ Global
+ Non-global


#### Global attributes

Global attributes can be applied to __all tags__. They are common attributes. Examples of global attributes are id and class. There are many more global attributes. Here is a [list of all the global attributes](https://www.w3.org/wiki/HTML/Attributes/_Global) and the values they accept. 

So attributes like `id` and `class` can be applied to any HTML tag.
<pre style="padding-left: 30px;"><span style="line-height: 25.6px;">&lt;p id="para1" class="poetry" lang="en"&gt;The global attribute lang takes language codes for values. The code for English is 'en'.&lt;/p&gt;<br><br>&lt;html lang="fr"&gt;&lt;/html&gt; </span>- The language attribute tells the browser that the contents of this document will be in french.</pre>


#### Non-global attributes

Non-global attributes are attributes applied to a specific instance of a tag. It can be applied to one or more tags. For example, `start` is an attribute for the `<ol>` tag and it cannot be applied on the `<p>` or `<h1>` tags, it is specific to only ordered lists `<ol>`. Another attribute specific to the `<ol>` tag is reversed, which we learned in the last unit as an example of a boolean attribute. The non-global attribute width can be applied to several tags such as `<img>`, `<input>` and `<video>`.

Without the boolean attribute `reversed`:

```html
<ol>
   <li>HTML5</li>
   <li>CSS</li>
   <li>JavaScript</li>
</ol>
```

With the boolean attribute reversed:

```html
<ol reversed>
   <li>HTML5</li>
   <li>CSS</li>
   <li>JavaScript</li>
</ol>
```

[Example Code](src/2.2.2-Attributes.html)

Ordered lists have their own specific attributes and all global attributes can also be applied to them.


#### More examples

The image `<img>` and hyperlink `<a>` elements, which we will be learning about shortly, have many non-global attributes of their own.

<strong>&lt;img&gt;</strong>  :  `src`, `alt`, etc.

<strong>&lt;a&gt;</strong>  : `href`, `target`, `download`, etc.

Other than the common global attributes, if you wish to learn about the supported non-global attributes for any element, you can visit the [W3C HTML5 recommendation](https://www.w3.org/TR/html5/dom.html#global-attributes) or the [HTML attribute reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes) available at the Mozilla Developer Network (MDN).

__Important__: Throughout the course, using the MDN attribute reference, you are encouraged to explore non-global attributes for the elements you learn about or would like to use in your Web pages. In the MDN attribute reference list, you can click on the element's hyperlinked name to be navigated to its page that lists supported attributes for that element.

__Try this__: Navigate to the [HTML attribute reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes) at Mozilla Developer Network and find out which element(s) the attributes muted and readonly can be applied to. 

__Try this__: Navigate to the [HTML attribute reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes) at Mozilla Developer Network and find out the non-global attributes that can be applied to the `<li>` tag. If you click on the `<li>` element, it will take you to the list tag's page that specifies applicable attributes.


### Global attributes: examples

#### Global attribute: 'id'

Like we saw in the previous unit, here is a [list of all the global attributes](https://www.w3.org/TR/html5/dom.html#global-attributes) and the values they accept. To understand attributes, we considered an example of usage `id` and `class`. We are going to look at it in depth here and discuss another global attribute `title`.

The id attribute gives your element a unique identifier. In your HTML document, that ID value can only be used in one element. 

Naming rules for `id` attribute:

+ Must be of at least one character
+ Should not contain any spaces
+ Values are case-sensitive. This means 'QuestioN' and 'question' are NOT the same. That does not mean you can use two different IDs that only differ by case, i.e. "myid" and "MyId". They are different and so legal but extremely confusing!

```html
<p id="question-about-html">How many times can a particular 'id' value be used in a HTML document?</p>
<p id="html-answer">Once</p>
```

`id` is primarily used for:

1. Styling your element. You can specify the style you want for the element in your style sheet by referencing the 'id'.

  Using CSS, you can specify code that will give different styles to "question-about-html" (eg: black text, center-aligned) and "html-answer"  (eg: green text)

2. Specifying a link target. We will be learning about hyperlinks later in this section. You can link to a section of your HTML page using the 'id' of the section. You should reference the 'id' value with a number sign preceding it - '#id-value'

  ```html
  <a href="#introduction">1.1 Introduction</a> 
    <!-- This is a hyperlink element which we will learn about later in this week -->
  <p id="introduction">This paragraph is the Introduction to the Web page</p>
  ```

3. In JavaScript, 'id' can be used to manipulate an html element. Using the 'id' of the element, you can write JavaScript code to make it perform an action, i.e. change the text within paragraph tags.


#### Global attribute: 'class'

The class attribute, while similar to id, groups a set of elements in the same class. It's name-value pair is class="classname". Unlike id, which is unique to the element,  the same class name can be assigned to more than one element.

For example:

```html
<p class="question">What is your name?</p>
<p class="question">Do you like HTML5?</p>
```

Both paragraphs above are grouped under the class named 'question'. An element can have one or more class names. If we also want the second question to be under the 'html' class because it is a html related question, you can add two class names by separating them by space:

```html
<p class="question html">Do you like HTML5?</p>
```

Naming rules for `class` attribute:

+ Must begin with a letter (a-z or A-Z)
+ First letter can be followed by a letter, digit, hyphen or underscore
+ Values are case-sensitive

class is primarily used for:

1. Styling your elements. You can specify the style you want for all the elements that belong to the class in your stylesheet. 

  ```html
  <p class="question">Who are you?</p>
  <p class="answer">I am the author</p>
  <p class="question html">Do you like HTML5?</p>
  <p class="answer">Yes</p>
  ```

  In your CSS, you can include code to style your classes like this:

  + 'question' class: text color is black and text is bold
  + 'answer' class: text color is green
  + 'html' class: text color is red

  The code above will look like this:

  <p style="padding-left: 60px;"><strong><span style="line-height: 25.6px;">Who are you?</span></strong></p>

  <p style="padding-left: 60px;"><span style="line-height: 25.6px; color: #339966;">I am the author</span></p>

  <p style="padding-left: 60px;"><span style="color: #ef0000;"><strong>Do you like HTML5?</strong></span></p>

  <p style="padding-left: 60px;"><span style="color: #339966;">Yes</span></p>

  The 'Do you like HTML5?' question has styles for both classes 'question' and 'html' applied to it.

2. In JavaScript, `class` can also be used to manipulate html elements of the same class. 


#### Global attribute: 'lang'

The lang attribute indicates the language of the text in the element to which it is attached.  Identifying the language of content is increasingly important, as browsers adapt styling and other aspects of the user's experience according to the language of the content. 

For example, if you create a page in Japanese, the browser will automatically apply a font that produces Japanese shapes for the characters, rather than Chinese shapes – but only if you have told it that your content is in Japanese. Various presentational aspects also require a knowledge of the language of the content: for example, CSS will style content differently for line-breaking, hyphenation, and text-transforms depending on the declared language. Other features, such as spell-checking and voice-browsers for visually-challenged people, also work differently according to which language the content is in.  For more details see [Why use the language attribute?](https://www.w3.org/International/questions/qa-lang-why)

The value of a lang attribute must be a language tag that is composed of one or more subtags defined in the [IANA Language Subtag Registry](http://www.iana.org/assignments/language-subtag-registry). Multiple subtags are separated by hyphens.  (Do n__ot use the ISO lists of languages and countries! Those lists are already subsets of the IANA registry.) You may find it easier to look up subtags using the unofficial [Language Subtag Lookup](https://r12a.github.io/app-subtags/) tool.

You should __always declare the language of your page in the `<html>` tag__.  You can also declare the language of content within the page by attaching a lang attribute to an element that surrounds it.

For example:

```html
<html lang="en-GB">...</html>
<p>In French you'd say <span lang="fr">On voit souvent des chats sur le Web.</span></p>
```

The first example above shows how you can qualify the language (English) with a region subtag (GB) to specify British English.  This distinction can be useful for spellchecking your source. You can also add other subtags, such as scripts and variant labels to further refine the language. However, the golden rule is to always keep the lang value as short as possible, and only use additional subtags when you have a good reason (ie. use just ja for Japanese, not ja-JP). For more information, see the article [Declaring language in HTML](https://www.w3.org/International/questions/qa-html-language-declarations).

The second example shows how you could specify a change of language within the document.  This would help a voice browser pronounce the French word 'chats' correctly, meaning 'cats' and not 'chats' in English.


#### Global attribute: 'title'

Try this: Place your cursor on the word and then on the picture below. Don't click on it, just rest your cursor there. 

Example image of a girl with a beautiful smile to illustrate title attribute

Did you see the two secret messages? A message that appears when you point your cursor at something is called a tooltip. Be it a paragraph, header, image or any element, the title attribute is used to provide additional information about it. It is very useful to elaborate abbreviations or add some context. For images, you must use an alt attribute as there is no guarantee that the title attribute is presented to assistive technology users. The title can be of any text value. 

```html
<abbr title="National Aeronautics and Space Administration">NASA</abbr>
```

#### Knowledge check 2.2.3

```html
<p id="greeting" class="hello world">This is me greeting the world</p>
```

Which of the following is the correct behavior with respect to the code above?

1. Both the classname and paragraph text cannot contain "world"
2. Two different classes "hello" and "world" will be applied to the paragraph
3. The code is invalid because space is not allowed in class attribute's value
4. One class "hello world" will be applied to the paragraph

  Ans: 2 <br/>
  Explanation: If there is a space between classes, they will be treated as two different classes - "hello" and "world". In this case, both classes will be applied to the paragraph.
  

### Global attributes

References for video below:

+ [W3C Cheatsheet](https://www.w3.org/2009/cheatsheet/)
+ [MDN Attribute Reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes)

<video src="https://edx-video.net/W3CHTM50/W3CHTM502016-V005600_DTH.mp4" preload="none" loop="loop" controls="controls" style="margin-left: 2em;" muted="" poster="http://www.multipelife.com/wp-content/uploads/2016/08/video-converter-software.png" width="180">
  <track src="https://courses.edx.org/courses/course-v1:W3Cx+HTML5.0x+1T2019/xblock/block-v1:W3Cx+HTML5.0x+1T2019+type@video+block@17f73d8ba52c4569967a94db806240a0/handler/transcript/download" kind="captions" srclang="en" label="English" default>
  Your browser does not support the HTML5 video element.
</video><br/>


### Activities - Attributes

Please find below suggested activities to help you practice:

1. Find the list of supported attributes for the `<area>` tag. (Hint: use the [W3C cheatsheet](https://www.w3.org/2009/cheatsheet/) or [MDN attribute reference list](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes))

  Attributes: alt, coords, ping, referrerpolicy, rel, shape, target

2. Create two paragraphs with the same `id` and run your code in a CodePen. What happens? We know the value of the `id` attribute must be unique, so why does it behave the way it does? Run your code through the [W3C Markup Validator](https://validator.w3.org/#validate_by_input). Does it throw an error?

  [Example code](src/2.2.5-AttributesID.html)

  ```txt
  Error: Duplicate ID idtest.
  </p>↩↩  <p id="idtest">Method
  ```

3. Does an attribute called `src` exist? What is the purpose of this attribute and what are the elements it can be applied to? (Hint: refer to the [W3C HTML5 specification](https://www.w3.org/TR/html5/index.html#contents), [W3C cheatsheet](https://www.w3.org/2009/cheatsheet/) or [MDN attribute reference list](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes))

  + src: The URL of the embeddable content; Valid non-empty URL potentially surrounded by spaces
  + Elements: audio, embed, iframe, img, input, script, source, track, video

4. Create an ordered list starting with the number 11. Then, reverse the list. Give it the following title (when you hover your mouse, it should display the title as a tooltip): 'Activity List'.

  [Example Code](src/2.2.5-ArttributesList.html)

Note: If you wish to share your HTML code in the discussions, you can paste your code directly in a discussion forum post (highlight code and Ctrl+K/use the code widget) or use one of the following online code editors:

+ JS Bin: http://jsbin.com (JS Bin tutorial)
+ CodePen: http://codepen.io (CodePen tutorial)

These are HTML, CSS, and JavaScript code editors that preview/showcase your code bits in your browser. It helps with cross-device testing, realtime remote pair programming.



## 2.3 Semantic meaning

### Separating content & style

When writing in hypertext language, it is important to separate content and style. Style should be kept tucked away in Cascading Style Sheets (CSS).

Let's look at a few interesting tags that lived as exception to this rule and were eventually corrected in HTML5.

+ `<p>This text is in <i>Italics</i>. It uses the i tag</p>`
+ `<p>This text is also in <em>Italics</em>. But it uses the em tag!</p>`
+ `<p>This text is in <b>Bold</b>. It uses the b tag</p>`
+ `<p>This text is also in <strong>Bold</strong>. But it uses the strong tag!</p>`

This is how the above [HTML code](src/2.3.1-Style.html) will look in a browser (go ahead and try it!)

It seems redundant for two tags to do the same thing in HTML. While `<b>` and `<strong>`, `<i>` and `<em>` seem no different in a regular Web browser there is an important difference between them.


#### Semantic vs Style tags

The four tags we saw above can be categorized into style and semantic tags.

Style tags, in HTML4, focused purely on presentation and design. It only talked about how the text should look like on the screen. 

Semantic refers to the meaning of words in a language. __Semantic tags__ said something about the semantic of the tag. It offered meaning. 

<table style="font-family: arial,helvetica,sans-serif; width: 60vw;" auto="" cellspacing="0" cellpadding="5" border="1" align="center">
<tbody>
  <tr>
    <td style="background-color: #3d64ff; color: #ffffff;">Tag</td>
    <td style="background-color: #3d64ff; color: #ffffff;">Type</td>
    <td style="background-color: #3d64ff; color: #ffffff;">Description</td>
  </tr>
  <tr>
    <td>&lt;b&gt;</td>
    <td>Style</td>
    <td>Makes text bold</td>
  </tr>
  <tr>
    <td>&lt;i&gt;</td>
    <td>Style</td>
    <td>Makes text italics</td>
  </tr>
  <tr>
    <td>&lt;em&gt;</td>
    <td>Semantic</td>
    <td>Emphasizes text<br><br>Text is italics by default in a browser</td>
  </tr>
  <tr>
    <td>&lt;strong&gt;</td>
    <td>Semantic</td>
    <td>Important text<br><br>Text is bold by default in a browser</td>
  </tr>
</tbody>
</table>


##### 'b' vs 'strong'

__Bold__ is a style that makes letters thicker so it stands out among other text but it has no semantic meaning, for example for voice browsers, screen readers, and other types of ways to access the Web. A device like [Kindle Paperwhite](https://en.wikipedia.org/wiki/Amazon_Kindle#Kindle_Paperwhite_.281st_generation.29) that renders text differently, might not pick up the bold.

__Strong__ is an indication of how something should be. It looks like bold in a browser, but it could mean ‘speak with urgency or seriousness’ when reading text aloud. It is semantic in the sense, that we instruct it to be stronger than the text it surrounds which is different from giving instructions on how the text should look in the case of `<b>`. It represents importance, seriousness, or urgency for its contents.

```html
<p>As a junior developer, you <strong>must</strong> submit your work for code review!</p>
```

The 'must' maybe be bolded in a browser. But when reading the HTML document out loud by a text-to-speech program, it can be spoken with importance or seriousness.


##### 'i' vs 'em'

__Italics__ slants text. We usually italicize names of magazine, books, TV shows etc. Just like the bold tag, since it is meant purely for presentation purposes, it means nothing to someone who cannot read the text.

__Emphasis__ is used to stress emphasis of its contents. The word in a sentence you emphasize can change the whole meaning. Try reading the sentences below out loud, stressing on the emphasized words: 'you' and 'store'. 

<p><i>You</i> have to go to the store.</p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Not me. That’s your job!&nbsp;</p>
<p>&nbsp;You have to go to the <i>store.</i></p>
<p>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp;To the store. Not the arcade.</p>


#### Changes in HTML5

So far, we have looked at how these tags were in HTML4. In the beginning of this unit, we learned that content and style should be kept separate and that styling should be kept tucked away in Cascading Style Sheets. So how did `<i>` and `<b>`, purely style elements make the cut? 

They were initially deprecated, however, in HTML5, they were brought back. This time, with semantic meaning. 

<table align="center" style="font-family: arial,helvetica,sans-serif;" border="1" cellspacing="0" cellpadding="5" table-layout="auto">
<tbody>
  <tr>
    <td width="30">&lt;i&gt;</td>
    <td>Apart from italic text, it is now also used for text in a different mood or voice, such as foreign words, a thought or technical terms.</td>
    <td>&lt;p&gt;This restaurant has a breakfast buffet and a four course <b style="color: #ff3300;">&lt;i lang="fr"&gt;</b>À la carte<b style="color: #ff3300;">&lt;/i&gt;</b> dinner.&lt;/p&gt;</td>
  </tr>
  <tr>
    <td width="30">&lt;b&gt;</td>
    <td>Apart from bolded text, it is now also used as a stylistic offset such as keywords in a document, product names or action words without making them as important. It can also be used as headings in list items.</td>
    <td>&lt;p&gt;The owner of this <b style="color: #ff3300;">&lt;b&gt;</b>rabbit<b style="color: #ff3300;">&lt;/b&gt;</b>and <b style="color: #ff3300;">&lt;b&gt;</b>hamster<b style="color: #ff3300;">&lt;/b&gt;</b> needs to step forward.&lt;/p&gt;</td>
  </tr>
</tbody>
</table>

As of HTML5, `<em>` is now also used for words and sentences you would pronounce differently. It is not used to convey importance. For that you should use `<strong>`.

You can nest both `<em>` and `<strong>`. Two `<em>` means higher level of stress/emphasis on the content than one `<em>`.

You should also bear in mind that `<b>` and `<i>` may not produce appropriate styling for some parts of the world. For example, Chinese characters are so complicated that they often prefer something such as underlining to bold, because bold makes it too difficult to read the text.

If you do use `<b>` or `<i>` tags, the HTML5 specification recommends that you also use class attributes to identify the semantic intention of the markup. This can be particularly important for pages that get translated, since styling doesn't necessarily map to the same semantic categories across different cultures. For more information, read the article [Using `<b>` and `<i>` elements](https://www.w3.org/International/questions/qa-b-and-i-tags).


#### Knowledge check 2.3.1

```html
<....> You need to leave immediately. Your office is bugged! <....>
```

Which of the following tags should be used in this case?

1. < strong >
2. < i >
3. < b >
4. < em >

  Ans: 1 <br>
  Explication: This text sounds like an important message spoken with urgency. 
  + The `<strong>` tag should be used for text that is typically spoken with urgency or seriousness.
  + `<em>` is used for emphasis but not to convey importance.


### Introduction to semantic elements

Semantic HTML is HTML that concentrates on the meaning of information in Web pages instead of its presentation or look.


#### What are semantic elements?

If you want to add a paragraph, you would use the paragraph tag. If you want to add a heading, you would use the header tags `<h1>`-`<h6>`, and to add an image, you would use the image tag (we will learn about this later in this module). All these tags along with their id and class attributes are semantic because they suggest the purpose of the content within the tags. `<i>` and `<b>` suggest nothing about the content and this is why they were not considered semantic enough and initially deprecated.


#### Using the right tags

From a semantic HTML perspective, using the right tags is important. You should use `<blockquote>` to wrap a quote and not use a paragraph tag and then style it to look like a quote. You should use `<em>` to emphasize a part of your content, not just to italicize text. For presentation purposes, you can achieve the same using CSS. How something looks has very little to do with what it means. This is why in HTML, we separate content and style.


#### Why is it important?

Semantic elements are beneficial to both the developer and browser. They convey much more information about your HTML document's content and structure. There is a tag called header in semantic HTML. When you see a heading like `<h1>` or `<h2>`, you know this is likely the start of a new sub-section or topic. Communication is always welcome in any programming language.

This additional communication is useful for a __developer__ who can understand the markup structure better (when you come back to your code after a year or pass it on to a colleague, this is going to help you and them a lot!). For the __browser__, it can better differentiate different types of data which results in better display of content in different devices. __Assistive technology__, such as a screen reader, will read content and convey information about the content depending on the semantic meaning, for example, identifying headers and reading them in a different tone.

Since its establishment, it is an ongoing effort on part of W3C to make HTML as semantic as possible. HTML5 brought with it a slew of new semantic elements.


#### Web page structure

Let's look at a typical Web page structure.

<div style="display:flex;justify-content:center;align-items:center;flex-flow:row wrap;">
  <div><a href="https://courses.edx.org/courses/course-v1:W3Cx+HTML5.0x+1T2019/courseware/7e7a7ad104714c61b5b7bd35048b9ddc/dd9cc2d025bc4ac5b1a66481aac0db1b/1?activate_block_id=block-v1%3AW3Cx%2BHTML5.0x%2B1T2019%2Btype%40vertical%2Bblock%4025b7c2657986416785cb4a8bb92fbfd2">
    <img src="https://prod-edxapp.edx-cdn.org/assets/courseware/v1/e8f770a8ceaa0d77fcf563e7633d64f8/asset-v1:W3Cx+HTML5.0x+1T2019+type@asset+block/site-structure-complex.jpg" style="margin: 0.1em;" alt="Website Structure" title="Website Structure" width="300">
  </a></div>
</div>

Do you see how each section refers to a part of the document?

<div style="display:flex;justify-content:center;align-items:center;flex-flow:row wrap;">
  <div><a href="https://courses.edx.org/courses/course-v1:W3Cx+HTML5.0x+1T2019/courseware/7e7a7ad104714c61b5b7bd35048b9ddc/dd9cc2d025bc4ac5b1a66481aac0db1b/1?activate_block_id=block-v1%3AW3Cx%2BHTML5.0x%2B1T2019%2Btype%40vertical%2Bblock%4025b7c2657986416785cb4a8bb92fbfd2">
    <img src="https://prod-edxapp.edx-cdn.org/assets/courseware/v1/d4a392ddecb2dcc4b9a4c9efa613e6f3/asset-v1:W3Cx+HTML5.0x+1T2019+type@asset+block/structurecalledout-new.jpg" style="margin: 0.1em;" alt="Diagram explaining basic web page tags" title="Diagram explaining basic web page tags" width="550">
  </a></div>
</div>

Tags such as `<article>`, `<section>`, `<header>`, `<nav>` and `<footer>` were specifically introduced in HTML5 to define the Web page structure. These new semantic elements give meaning to different parts of a webpage. When you do a Google search, the search engine automatically processes millions of HTML pages to scan and offer you the most appropriate content.

The use of these semantic elements improves the __automated processing of documents__. When it scans a `<nav>` tag, it automatically knows it includes content related to page navigation or a header indicates introductory content. It provides the structure and consistent behavior across many webpages providing simpler and more direct information to browsers making life easier for them. It also improves the __accessibility__ of webpages. Assistive technologies depend on the structure of the document to present information to the users. If a screen reader can correctly determine the structure of a document, it reads the document more seamlessly and avoids irrelevant information or repeating content.

We can apply the elements in the image above to a simple Web page like [this](src/2.3.2-SimpleWeb.html)


#### Knowledge check 2.3.2

Why should you use semantic elements in your Web page?

1. It provides meaning and structure to the Web page and improves automated processing of documents
2. A user will eventually run out of 'id' values and semantic elements solve that problem
3. It makes styling the Web page easier
4. It will drastically improve the structure of your document visually

  Ans: 1<br/>
  Explanation: Semantic elements provide more meaning and structure to the information in Web pages instead of its presentation or look. It is used to improve processing of documents by the browser and search engines.


### New HTML5 semantic elements

We will elaborate on selected semantic elements in detail in the next unit.

<table style="font-family: arial,helvetica,sans-serif;" table-layout="auto" cellspacing="0" cellpadding="5" border="1" align="center">
<tbody>
  <tr>
    <td style="background-color: #3d64ff; color: #ffffff;" width="70">Semantic Element</td>
    <td style="background-color: #3d64ff; color: #ffffff;">Description</td>
    <td style="background-color: #3d64ff; color: #ffffff;">Example</td>
  </tr>
  <tr>
    <td width="90"><strong>&lt;header&gt;</strong></td>
    <td>Introduction for the whole page or individual sections, article, nav, aside elements. Typically contains site name, logo, navigation. Does not have to be at the  beginning of page.</td>
    <td>&lt;header&gt;<br> &lt;h1&gt;The Importance of Being Earnest&lt;/h1&gt;<br> &lt;h3&gt;A Quest for Truth and Beauty&lt;/h3&gt;<br> &lt;p&gt;The play was written in 1895 by playwright Oscar Wilde&lt;/p&gt;<br>&lt;/header&gt;</td>
  </tr>
  <tr>
    <td width="90"><strong>&lt;footer&gt;</strong></td>
    <td>Includes typical footer information like authoring, copyrights, contact information and a footer menu.</td>
    <td>&lt;footer&gt;<br> &lt;p&gt;Written by: Oscar Wilde&lt;/p&gt;<br> &lt;p&gt;Contact information: &lt;a href="mailto:oscar@wilde.com"&gt;<br> oscar@wilde.com&lt;/a&gt;.&lt;/p&gt;<br>&lt;/footer&gt;</td>
  </tr>
  <tr>
    <td width="90"><strong>&lt;nav&gt;</strong></td>
    <td>Navigation links for the document. A page can have more than one &lt;nav&gt; element like table of contents, horizontal navigation in header and footer navigation.</ td>
    <td>&lt;nav&gt;&lt;ol&gt;<br>&lt;li&gt;&lt;a href="/act1/"&gt;Act 1&lt;/a&gt;&lt;/li&gt;<span style="line-height: 1.6;">&nbsp;&nbsp;</span><br><span style="line-height: 24.8889px;">&lt;li&gt;</span>&lt;a href="/act2/"&gt;Act 2&lt;/a&gt;&lt;/li&gt; <br><span style="line-height: 24.8889px;">&lt;li&gt;</span>&lt;a href="/act3/"&gt;Act 3&lt; /a&gt;&lt;/li&gt;<br>&lt;/ol&gt;&lt;/nav&gt;</td>
  </tr>
  <tr>
    <td width="90"><strong>&lt;section&gt;</strong></td>
    <td>Defines sections in&nbsp;the document&nbsp;such as&nbsp;chapters, headers, etc. Typically used on content that cannot make sense on its own.&nbsp;</td>
    <td>&lt;section&gt;<br> &lt;h1&gt;Act 1 - Scene 1&lt;/h1&gt;<br> &lt;p&gt;Set in the morning room of Algy's flat in Half Moon Street&lt;/p&gt;<br>&lt;/section&gt;</td>
  </tr>
  <tr>
    <td width="90"><strong>&lt;article&gt;</strong></td>
    <td>Defines independent content that should make sense on its own outside of the document&nbsp;such as&nbsp;newspaper articles, blog posts, etc.</td>
    <td>&lt;article&gt;<br> &lt;h1&gt;A blogger's analysis of this brilliant satire&lt;/h1&gt;<br> &lt;p&gt;This witty, sometimes conscious play is Wilde's playground to   raise his progressive sentiments...&lt;/p&gt;<br>&lt;/article&gt;</td>
  </tr>
  <tr>
    <td width="90"><strong>&lt;aside&gt;</strong></td>
    <td>Side content other than main content, like a sidebar. These are not considered as part of the main page outline.</td>
    <td>&lt;p&gt;Algernon's flat is luxuriously and artistically furnished&lt;/p&gt;<br><br>&lt;aside&gt;<br> &lt;h3&gt;Algernon Moncrieff&lt;/h3&gt;<br> &lt;p&gt;A wealthy bachelor who lives in a fashionable part of London. He has a good sense of humor and utter lack of respect for society.&lt;/p&gt;<br>&lt;/aside&gt;</td>
  </tr>
  <tr>
    <td width="90"><strong>&lt;details&gt;</strong><br><br><mark>*see example below</mark></td>
    <td>A way to provide additional information that the user can show or hide. Content that is shown to user by default. Other content is hidden and can be expanded to  view.</td>
    <td>&lt;details&gt;<br> &lt;summary&gt;Cast Members&lt;/summary&gt;<br> &lt;p&gt;George Washington as Algernon Moncrieff&lt;/p&gt;<br> &lt;p&gt;Ronald Reagan as John Worthing&lt;/p&gt;<br>&lt;/details&gt;</td>
  </tr>
  <tr>
    <td>
      <p width="90px"><strong>&lt;figcaption&gt;</strong></p>
      <p><span style="line-height: 22.4px;"><mark>*see example below</mark></span><strong></strong></p>
    </td>
    <td>Provides a caption (explanation) of an image. To be used within &lt;figure&gt;.</td>
    <td>&lt;figure&gt;<br> &lt;img src="img_cast.jpg" alt="The Importance of Being Earnest Cast"&gt;<br> &lt;figcaption&gt;Fig1. - The cast hard at work at dress rehearsal before opening night&lt;/figcaption&gt;<br>&lt;/figure&gt;</td>
  </tr>
  <tr>
    <td width="90"><strong>&lt;figure&gt;</strong></td>
    <td>Contains an image and can be used to group with an image's caption</td>
    <td>Refer to &lt;figcaption&gt;</td>
  </tr>
  <tr>
    <td>
      <p width="90px"><strong>&lt;mark&gt;</strong></p>
      <p><span style="line-height: 22.4px;"><mark>*see example below</mark></span><strong></strong></p>
    </td>
    <td>Defines a part of a text you want to highlight. The highlight styling is specified in CSS.</td>
    <td>&lt;h4&gt;Lane: &lt;/h4&gt;&lt;p&gt;Yes sir. [&lt;mark&gt;Handing his master the sandwiches on a salver&lt;/mark&gt;]&lt;/p&gt;</td>
  </tr>
  <tr>
    <td width="90"><strong>&lt;summary&gt;</strong></td>
    <td>Used within the &lt;details&gt; tag. Specifies the visible content. The rest of the content in details is shown/hidden by user.</td>
    <td>&lt;details&gt;<br> &lt;summary&gt;Cast Members&lt;/summary&gt;<br> &lt;p&gt;George Washington as Algernon Moncrieff&lt;/p&gt;<br> &lt;p&gt;Ronald Reagan as John   Worthing&lt;/p&gt;<br>&lt;/details&gt;</td>
  </tr>
</tbody>
</table>


#### 'details' element

The `<details>` tag is very cool. It is used in conjunction with a nested `<summary>` tag and some other content. The result is that the summary is shown with a disclosure triangle alongside it, and the other content is initially hidden.  By clicking the triangle, the other content is displayed to the user. This requires no JavaScript and is a simple way to get a powerful and desirable feature.

Below we see the HTML, and you can try it out for yourself! Note that the `<details>` tag works in most Web browsers.

<table>
<tbody>
  <tr><th>HTML</th><th style="width: 300px;">Result / Try It!</th></tr>
  <tr>
    <td>
      <div style="padding-left: 30px; padding-right: 30px;border: 1px solid black;"><ol>
        <li class="L0" style="margin-bottom: 0px;" value="1"><span style="color: #008;">&lt;details&gt;</span></li>
        <li class="L1" style="margin-bottom: 0px;"><span style="color: #000;">&nbsp;&nbsp; </span><span style="color: #008;">&lt;summary&gt;</span><span style="color: #000;">Cast Members</span><span   style="color: #008;">&lt;/summary&gt;</span></li>
        <li class="L2" style="margin-bottom: 0px;"><span style="color: #000;">&nbsp;&nbsp; </span><span style="color: #008;">&lt;p&gt;</span><span style="color: #000;">George Washington as Algernon  Moncrieff</span><span style="color: #008;">&lt;/p&gt;</span></li>
        <li class="L3" style="margin-bottom: 0px;"><span style="color: #000;">&nbsp;&nbsp; </span><span style="color: #008;">&lt;p&gt;</span><span style="color: #000;">Ronald Reagan as John Worthing</ span><span style="color: #008;">&lt;/p&gt;</span></li>
        <li class="L4" style="margin-bottom: 0px;"><span style="color: #008;">&lt;/details&gt;</span></li>
      </ol></div>
    </td>
    <td><details><summary>Cast Members</summary>
      <p>George Washington as Algernon Moncrieff</p>
      <p>Ronald Reagan as John Worthing</p>
    </details></td>
  </tr>
</tbody>
</table>

<details open=""> element</details>


[Example Code](src/2.3.3-details.html)

See also the current [browser support](http://caniuse.com/#search=%3Cdetails%3E) (on caniuse.com).


#### 'figcaption' element

This element is used to provide a caption or explanation of the image (figure). While the alt attribute explains the image for assistive technology, `<figcaption>` can be used to provide additional information for all users.

```html
<figure>
   <img src="img_cast.jpg" alt="The Importance of Being Earnest Cast">
   <figcaption>Fig1. - The cast hard at work at dress rehearsal before opening night</figcaption>
</figure>
```

Result:

<figure>
  <img width="300" alt="dress rehearsal" src="https://prod-edxapp.edx-cdn.org/assets/courseware/v1/8b8ca4b537a667b251cb45f6ec8aab7b/asset-v1:W3Cx+HTML5.0x+1T2019+type@asset+block/dressrehears.jpg" type="saveimage" target="[object Object]"><br>
  <figcaption>Fig1. - The cast hard at work at dress rehearsal before opening night</figcaption>
</figure>


#### 'mark' element

This element is used to specify content that you want to highlight. 

```html
<h3>Lane: </h3><p>Yes sir. [<mark>Handing his master the sandwiches on a salver</mark>]</p>
```

[Example Code](src/2.3.3-mark.html)

Most browsers will display mark element with a yellow background to black text by default, however, if it doesn't, you can specify the styling in CSS. See also the current browser support (on caniuse.com).


#### Effect of semantic elements

If you have had a chance to try the examples of the semantic elements discussed above, you will notice that semantic elements are not visually promising in general. Only a few semantic elements such as `<mark>`, `<em>`, `<strong>` and `<code>` provide some kind of visual change to the document. The rest don't do anything except providing the structure for your document. 

A good example is `<aside>`. The `<aside>` element is used for side content other than the main content, such as a sidebar, but it does not actually create a sidebar in your page. Sidebar is a user interface (UI) element and must be styled to achieve the look of a sidebar. The following code will only create structure to your document, not any visual change:

[Example Code](src/2.3.3-Effect.html)


#### Lesser known semantic elements

Note: This section is optional material included for the curious. It will not appear on any graded question.

We will look at a few more semantic elements that are commonly in use but lesser known.

<table style="font-family: arial,helvetica,sans-serif;width: 70vw;" align="center" cellspacing="0" cellpadding="5" border="1">
<tbody>
  <tr>
    <td style="text-align: center; background-color: #3d64ff; color: #ffffff; width: 10%;">Semantic Element</td>
    <td style="text-align: center; background-color: #3d64ff; color: #ffffff; width: 30%;">Description</td>
    <td style="text-align: center; background-color: #3d64ff; color: #ffffff; width: 30%;">Example</td>
  </tr>
  <tr>
    <td>&lt;code&gt;</td>
    <td>Used to represent short computer code in a sentence. It displays code in default monospace font.&nbsp;</td>
    <td>&lt;p&gt;For larger code snippets, you should use the &lt;code&gt;pre tag&lt;/code&gt;.&lt;/p&gt;</td>
  </tr>
  <tr>
    <td>&lt;abbr&gt;</td>
    <td>Used to indicate the occurrence of an abbreviation.</td>
    <td>&lt;abbr title="Hypertext Markup Language"&gt;HTML&lt;/abbr&gt;</td>
  </tr>
  <tr>
    <td>&lt;br&gt;</td>
    <td>Used to introduce a line break in your HTML document.</td>
    <td>&lt;br&gt;</td>
  </tr>
  <tr>
    <td>&lt;address&gt;</td>
    <td>Used to supply contact information for its nearest <code>&lt;article&gt;</code> or <code>&lt;body&gt;</code> ancestor.</td>
    <td>&lt;address&gt;<br>&lt;a href="www.example.com"&gt;John Doe&lt;/a&gt;&lt;br&gt;<br>#123, Doe Villa&lt;br&gt;<br>Los Angeles, USA<br>&lt;/address&gt;</td>
  </tr>
  <tr>
    <td>&lt;hr&gt;</td>
    <td>Used to introduce a horizontal line in your HTML document.</td>
    <td>&lt;p&gt;Hello&lt;/p&gt;&lt;hr&gt;&lt;p&gt;World!&lt;/p&gt;</td>
  </tr>
</tbody>
</table>

Apart from these, `<cite>`, `<em>`, `<strong>`, `<p>` and `<blockquote>` are also semantic elements.


#### Knowledge check 2.3.3

True of False? You are designing a Web page to store your grandmother's recipes. Each recipe should be enclosed in a `section` element.

  Ans: False<br>
  Explication: A page from a recipe book is independent content that will make sense on its own. Thus, the `article` element will be more appropriate.


### Differentiating semantic elements

Now, you have learned the semantic elements available and their syntax. When you try to apply it practically, there are some common problems you might run into. For example, when do we use `<header>` and when do we use `<h1>` to `<h6>` tags? Can I use semantic elements like `<header>`, `<footer>` and `<nav>` multiple times in my Web page? Or a more frequent question, do I use `<article>`, `<section>` or `<div>`?

Fear not. We will discuss these scenarios in detail so you can be better equipped to apply semantic elements in your Web page.


#### 'header' vs 'h1' - 'h6'

`<header>` is simply an area to add any introductory content about your page. It can contains headings, paragraphs, tables, images, logos and even navigation. `<h1>` to `<h6>` are headings we learned early on in the course. `<h1>` is for the most important heading and `<h6>` is for the least important. Let's see an example of how to use the `<header>` and `<h1>` to `<h6>` tags in your Web page.

For a simple HTML page, we will use the W3C HTML5 specification. You can view the page's source code on any browser by right-click and select 'view page source'.

If you view page source on the W3C specification and do a search for `<header>`, you will be able to view the contents of the header element. Here's a simplified version:

```html
<header>
   <!-- You will learn about the <a> and <img> tags later in this chapter-->
  <p>
    <a href="http://www.w3.org/"><img alt="W3C logo" height="48" src="http://www.w3.org/Icons/w3c_home" 
      width="72"></a>
  </p>
 
  <h1>HTML 5.2</h1>
  <h2>W3C Recommendation, 14 December 2017</h2>
</header>
```

[Example Code](src/2.3.4-header.html)

Like in the example above, the header can and frequently does contain headings `<h1>` to `<h6>`. In the case of headings, they do not have be to be used within a header.

__Important__: Headings are extremely helpful as a navigation tool for assistive technology users. While it is valid to skip header levels (have an h4 after an h2), it is not a good practice. Assistive technology often relies on the semantics of headings to understand your document's structure. More information is provided in [Using h1-h6 to identify headings](https://www.w3.org/TR/WCAG20-TECHS/H42.html).

[Example Code](src/2.3.4-h12h6.html)

Assistive technology uses heading markup, `<h1>` to `<h6>` to identify headings in a document. By using them to define your document's structure, a screen reader that parses your Web page will in some manner indicate the heading level. For example, raise its voice to indicate higher level headings or announce the heading level with the text it reads. They can also navigate through the headings quicker making it easier for the user to navigate contents of the Web page.

You can learn more about the source of this technique in that [other W3C resource page about headings](https://www.w3.org/WAI/tutorials/page-structure/headings/).


#### Can you have more than one 'header', 'footer' and 'nav'?

There is a common misconception that a Web page can only have one header at the start, one footer at the end and one main navigation section to maneuver the site. 


##### Multiple 'headers' & 'footers'

Header and footer elements are for the parent element (section, article, division or body) that they are used in. If you have multiple sections or articles, then you can have one header and footer for each.


##### Global 'header' & 'footer'

Header and footer elements can also be used site-wide at the top and bottom of the body of the Web page. This type of header will typically contain logos, main heading, a search area and site-wide navigation and the footer will typically include authoring information, references and other links, copyright information etc.

Sometimes, the header of a Web page comes from a template file. This template file is used throughout the site as a global header. Check out [this demo](http://demo.tutorialzine.com/2015/02/freebie-7-responsive-header-templates/) by tutorialzine.com for examples of header templates.

Let's look at site-wide/global header and footer used in [Microsoft Virtual Academy home page](https://mva.microsoft.com/). At the time of course creation, here are screenshots of its header  

<div style="display:flex;justify-content:center;align-items:center;flex-flow:row wrap;">
  <div><a href="https://courses.edx.org/courses/course-v1:W3Cx+HTML5.0x+1T2019/courseware/7e7a7ad104714c61b5b7bd35048b9ddc/dd9cc2d025bc4ac5b1a66481aac0db1b/1?activate_block_id=block-v1%3AW3Cx%2BHTML5.0x%2B1T2019%2Btype%40vertical%2Bblock%4025b7c2657986416785cb4a8bb92fbfd2">
    <img src="https://prod-edxapp.edx-cdn.org/assets/courseware/v1/367b933fb83e55ed9030bcb34715c0fb/asset-v1:W3Cx+HTML5.0x+1T2019+type@asset+block/MVA-header.png" style="margin: 0.1em;" alt="Screenshot of the MVA's home page header" title="Screenshot of the MVA's home page header" width="550">
  </a></div>
</div>

and footer.

<div style="display:flex;justify-content:center;align-items:center;flex-flow:row wrap;">
  <div><a href="https://courses.edx.org/courses/course-v1:W3Cx+HTML5.0x+1T2019/courseware/7e7a7ad104714c61b5b7bd35048b9ddc/dd9cc2d025bc4ac5b1a66481aac0db1b/1?activate_block_id=block-v1%3AW3Cx%2BHTML5.0x%2B1T2019%2Btype%40vertical%2Bblock%4025b7c2657986416785cb4a8bb92fbfd2">
    <img src="https://prod-edxapp.edx-cdn.org/assets/courseware/v1/298b40740c0f0b470e44b141e27d8433/asset-v1:W3Cx+HTML5.0x+1T2019+type@asset+block/MVA-footer.PNG" style="margin: 0.1em;" alt="Screenshot of MVA's home page showing the footer" title="Screenshot of MVA's home page showing the footer" width="550">
  </a></div>
</div>

If you visit the page and navigate to other parts of the site, you will see that the header and footer remain unchanged. 


##### Multiple navigation menus

So we know we can have the nav element in header. In the example above, we have one in the global header with menu items 'Courses'. Did you notice that we also have one in the footer? With menu items 'Support', 'Terms of Use', etc. You can definitely have more than one navigation menu in your Web page because there are so many different types of menus calling the need for multiple `<nav>` tags. Using `<nav>` also helps assistive technology. Screen readers now knows exactly where page navigation lies so it can provide options for the users to either skip reading its contents or to make it immediately available.


##### Complete example

Now, let's look at a more complete example using a global header and multiple `<header>`, `<footer>` and `<nav>` tags.

[Complete Example](src/2.3.4-complete.html)


#### Knowledge check 2.3.4

True or False? All headings should be used within the header element.

  Ans: False<br/>
  Explication: Headings, h1 to h6, need not be confined to the header element. They can be used throughout the document. You can include your primary page's heading and headings used at the start of your article or section within the header element.



### 'article' and 'section' elements

An article element as we know is stand-alone content. If you pick an article out of a Web page, it should make sense all by itself. In [Brad's Blog example](https://codepen.io/w3devcampus/pen/oWqbad) in the previous unit, if you extract only the first article, you can see that it will make sense all by itself without any context. It can be reused anywhere else.

```html
<article id="ces">
  <header>
    <h2>CES 2018</h2>
    <h3>Consumer electronics and consumer technology tradeshow</h3>
  </header>
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam neque risus,
    consequat eget vestibulum eu, consequat at eros. Nam eu nisl vel neque malesuada
    sollicitudin quis eget libero.</p>
  <footer>
    <p>Written by guest author Nicholas Abc. Read Nicholas's blog here.</p>
  </footer>
</article>
```

One article element can be nested inside another. For example, if you have a blog post and you want to include a forum post or newspaper article in it, you can nest it in another `<article>` tag.

Let's look at another example:

```html
<h4>Getting There</h4>
<p>Arriving at the show location proved much harder for me. I couldn't get a hotel
  closer to where the show was taking place and so had to rent a car....</p>
<h4>Conference Sessions</h4>
<p>I managed to squeeze in 3 conference sessions on the first day...</p>
```

This doesn't look like it makes sense all on its own. So we can't put it into an article element. Maybe a section element?

The __section element__ is used to section a page. For example, chapters in a book, sections in a thesis or splitting an 'about me' page into introduction, interests and skills. Sections can be used in a page or within an article. In fact, all content within the body element is considered to be within one section. Sections can be nested (one section in another). Sections can also be part of an article, aside or nav elements. While the code above makes no sense by itself, if you add it to our CES 2018 `<article>` example, it will fit right in.

[Example Code](src/2.3.5-ArticleSec.html)

An article element can use section elements to split its contents into groups.


#### Semantic elements sample

To get a better understanding on the usage of semantic elements in your Web page, try on this [CodePen](https://codepen.io/w3devcampus/pen/Wjzjpx)

[Semantic Element Complete Example](src/2.3.5-Semantic.html)

It is an example of an informational page about HTML5 using the following semantic elements: header, nav, main, article, section, aside, mark, figure, figcaption, details and summary.

Experiment with the sample and try inserting other semantic elements that you want to try.


#### Knowledge check 2.3.5

```html
<article id="main-content">
  <header>
    <h2>Tehnology Trends</h2>
    <h3>The best of tech in 2017</h3>
  </header>
  <p>Some cool info about technology...</p>
    <article id="sub-article">
      <header>
        <h3>Article on technology trends published by XXX magazine on August 2017</h3>
      </header>
      <p>XXX article content...</p>
    </article>
    <p>Some more cool info...</p>
</article>
```

Is the code above valid?

  Ans: Yes<br>
  Explanation: One article element can be nested inside another, i.e. a blog post can contain a newspaper article like in the example above.



### 'div' and 'span' elements

#### The 'div' tag

The `<div>` tag is one you will likely see sprinkled all over an HTML document. It is used to define a division or a section of the document. Div is not a semantic element, however, it is commonly used when there isn't a better semantic assignment for it.

It is like a __generic container__ that can hold a variety of elements such as paragraphs, images, links, tables, etc. It can be used to group elements for styling purposes. You can do this by assigning an `id` or `class` attribute to the div element and then apply styles which will affect all elements in the div container.

It should only be used if you cannot use any other semantic element in its place.

We will see an example of `<div>` here:

```html
<section>
  <h2>Week 1</h2>
  <p>This week, you will be learning about...week 1 stuff</p>
  <div class="code">
    <ol>
      <li>Line of code</li>
      <li>Line of code</li>
    </ol>
  </div>
</section>
<section>
  <h2>Week 2</h2>
  <p>This week, you will be learning about...week 2 stuff</p>
  <div class="code">
    <ol>
      <li>Line of code</li>
      <li>Line of code</li>
    </ol>
  </div>
</section>
```

If you want to style all code snippets in your HTML document a certain way, you can place your code in a div container and apply styles collectively to it using the `class` attribute.


#### The 'span' tag

While we are at the topic of the `<div>` tag and semantic elements, one more important element that comes in handy is `<span>`. Span and Div are so similar yet so different that there is an entire [wikipedia page](https://en.wikipedia.org/wiki/Span_and_div) dedicated to it.


##### Usage

What happens when you do not find an appropriate tag to use? Let's look at this example:

```html
<p>Hi everyone! My name is Alexa and I work for ABC Company</p>
```

I want to change the color of only 'ABC Company'? Should I use a paragraph tag? Let's try that..

```html
<p>Hi everyone! My name is Alexa and I work for <p class="company">ABC Company</p></p>
```

If you then design your style such that the 'company' class will make text blue, the output will look like this:

<p style="padding-left: 60px;">Hi everyone! My name is Alexa and I work for</p>

<p style="color: blue; padding-left: 60px;">ABC Company</p>

That does not work because `<p>` splits it into a newline. The HTML above is also invalid. We will see why shortly. Now, let's try `<span>`.

```html
<p>Hi everyone! My name is Alexa and I work for <span class="company">ABC Company</span></p>
```

Hi everyone! My name is Alexa and I work for <span style="color: blue;">ABC Company</span>


##### When can 'span' be used?

+ To add styling to part of a sentence (inline)
+ Manipulate part of a sentence using JavaScript
+ When no other HTML element is applicable, you can use `<span>` (and `<div>`) to add attributes such as class and id

Like `<div>`, `<span>` is not a semantic element. You should only use `<span>` if no other semantic element is appropriate. `<div>` and `<span>` serve the same purpose but should be applied at different levels. `<div>` is a block level element (for a block of space) while `<span>` is an inline element (for within a line or phrase).


#### Difference between 'div' and 'span'

They are both considered generic elements that don't have any meaning. But `<div>` is a block level element while `<span>` is an inline element. 

Block level elements - used within body of the page. It occupies a block of space and starts in a new line. It usually has an empty line above and below the block. They can contain inline elements and other block level elements. Other examples: `<p>`, `<h1>` - `<h6>`.

Inline elements - as the name suggests are 'in-the-line'. They can start anywhere in a line. They can only contain data (like text) or other in-line elements. Other examples: `<em>`, `<strong>`.

Note: There are several other semantic inline elements such as `<abbr>`, `<cite>` and `<code>` that should be used when possible instead of <span>.


#### Why two paragraph tags don't work

In the first `<span>` example, we said using two paragraph tags was invalid HTML.

```html
<p>Hi everyone! My name is Alexa and I work for <p class="company">ABC Company</p></p>
```

After an opening tag `<p>`, if it sees another `<p>` or any other block level element including `<div>`, it will automatically close the first open `<p>` for you. Nesting one paragraph tag in another is not valid because the browser will consider them as two paragraphs one after the other. Even though you close the paragraphs with two closing tags `</p></p>` at the end, they are ignored as errors.


#### Knowledge check 2.3.6

True or False? `<span>` should be used anytime you want to make inline changes

Ans: False, xTrue<br/>
Explication: `<div>` and `<span>` should only be used when no other semantic element is appropriate. If you can use inline semantic elements like `<abbr>`, `<cite>` and `<code>`, then they should be used in place in `<span>`.


### Activities - Semantic meaning

Please find below suggested activities to help you practice:

1. How are `<header>` and `<h1>` related? What is the difference between them?

  + `<header>`: simply an area to add any introductory content about your page.  It can contains headings, paragraphs, tables, images, logos and even navigation.
  + `<h1>` ~ `<h6>`: These elements represent headings for their sections. The semantics and meaning of these elements are defined in the section on headings and sections.

2. Create a well structured HTML page using as many semantic elements as you can.

  [HTML code](src/2.3.7-SemanticQ2.html)

3. Write a short HTML page that uses the `<div>` and `<span>` tags. You need not style them.

  [HTML Code](src/2.3.7-SemanticQ3.html)



## 2.4 Images

### Introduction to images


#### The 'img' Tag

In this age of visual culture, what is a Web page without images? Boring! Pictures and images make everything more interesting and engaging. 

Here is the most basic `<img>` tag:

```html
<img src="example.png" alt="Example Tutorial Image">
```

The image tag has several attributes out of which only src and alt are required. The rest are useful but optional attributes. 


##### Image: 'src' attribute

The source attribute from the `<img>` tag tells us where to fetch the image from. There are two different types of URLs you can give for source. 

1. Path to an image file within your Web site: 

  ```html
  <img src="images/image-with-relative-url.png" alt="Example Tutorial Image">
  ```

2. Path to an image file that resides elsewhere on the Web: 

  ```html
  <img src="http://www.example.com/image-with-absolute-url.png" alt="Example Tutorial Image">
  ```

The type of image file format (i.e. png, jpeg, etc.) you should use does not depend on the img element in HTML5 but on the browser that renders the content. Some formats like png, jpeg, gif and bmp are widely supported by browsers and so they are recommended when using images in your Web site. Here is a [comprehensive list by Wikipedia](https://en.wikipedia.org/wiki/Comparison_of_web_browsers#Image_format_support) listing browsers and the image formats they support.

Here is a list of things to keep in mind when using the src attribute:

+ Do not include spaces in your image path.
+ Make sure your image path matches the capitalization of the actual path. Your images directory in your Web project might be 'Images/' but your path might say 'images/' missing the capitalization in 'I'. Mismatched capitalization might work in some places but not all. Recommended practice: use lower case for all directories, file names and file extensions.
+ Use Unix (/) path name separator instead of Windows (\) style. This might work on Windows but will fail elsewhere. The path should be 'images/example.png' and not 'images\example.png'.
+ When your Web page loads, it is always going to look at the location you specified in src for the image. Ensure the image resides in the right location or the user is going to get a broken link. This is even more crucial when you use a relative path - any path that is 'relative to' the file. E.g. 'images/test.png' is going to look for the 'images' directory in the same level as your html page. Thus, you need to ensure your document root doesn't change. The simplest is to always keep the images at the same level, or one level down.
+ Absolute paths are not recommended to use because essentially, you are hardcoding the entire URL. The URL contains parts to it before the actual path - `http://example.com/images/test.png` like the protocol (http) and domain name (example.com). Whereas, relative URLs start with a path - '/images/test.png'. The base URL here comes from where your HTML document is deployed. This is easier to maintain. It will work on localhost or if you switch domain names without requiring any changes.


#### Image: Formats

Before you begin using images in your Web site, you are advised to visit this Web page to get an understanding of the most common image file types such as jpeg, gif, bmp, tiff and png, their pros and cons, operating system compatibility, when to use which format, etc. 

When using images in your HTML5, there are a few image format related information to be aware of.

+ __Image data__: most images, especially JPEG, contain a lot more data than is needed for a browser and are too often overly large and slow.  You can reduce the size of the image using photo editing software that allows you to re-sample an image to reduce its pixel data and in turn reducing image size. However, once you re-sample an image, do not make change its size (height and width) to make it larger as it will become pixelated and blurry.
+ __JPEG__ (Joint Photographic Experts Group) images compress well and are the standard for photos. But they don’t support any sort of animation or transparency.
+ __PNG__ (Portable Network Graphics) images support transparency and alpha channels. This makes them useful for non-rectangular images that may need to overlay different background colors or other elements on the page. To make PNG images, a user would need graphics editing software (like GIMP, Photoshop, or others). PNG is a [W3C Web standard](https://www.w3.org/TR/PNG/) (this is the 2nd edition - the 1st edition was [published](https://www.w3.org/TR/REC-png-961001) in 1996!).
+ __SVG__ (Scalable Vector Graphics) are defined mathematically and support animation. Also, since they are defined mathematically  they scale to Logo Scalable Vector Graphics (SVG) any size without worrying about pixels, resolution or image data. This makes SVG images an excellent format to use, if possible. SVG is great for charts, graphs, maps, geometric shapes, and line based illustrations.  SVG is also a markup language in its own right and is very similar to HTML. Typically, it is created with vector graphic software (like Inkscape, Adobe Illustrator, and [others](https://developer.mozilla.org/en-US/docs/Web/SVG/Tutorial/Tools_for_SVG)), but some people write the markup by hand. Note that SVG 1.1 is a [W3C Web standard](https://www.w3.org/TR/SVG/).


#### Knowledge check 2.4.1

What’s the best way to ensure that your picture will display correctly?

1. add the 'src' attribute
2. add the 'display' attribute
3. use an image file format commonly supported by browsers
4. change your HTML editor

  Ans: 3, x1<br/>
  Explanation: The browser support for image file format varies. You should use formats like png, jpeg and gif that are widely supported else you risk your image not displaying or displaying incorrectly.<br/> Submit Some problems have options such as save, reset, hints, or show answer. These options follow the Submit button.


### Attribute: alt

`alt` stands for alternate text for an image.

```html
<img src="image/example.png" alt="Add a short text description of the image here">
```

Using this attribute, you can provide a short description of what the image is about. This description should convey information about the image or its function in the page. The alt is an important attribute because it is the text alternative to the image for users who are unable to see the image, instead using assistive technology like screen readers that rely on the alt text.  It is also useful to provide relevant information for search engines.


#### Importance of THE 'alt' attribute

+ If you add alt to your image, screen readers will typically announce that there is an image and read out the contents of the alt attribute.
+ Your image will not display if the path in your source attribute is wrong, if you have a slow internet connection, or if the image has been relocated or renamed. It will show a broken link. It is useful to have the alternate text display so the user can make sense of the missing image.
+ Search engines do not 'see' images. They rely on the alt attribute to find out what the image is about. If you use your target keyword in alt, it will optimize the search.
+ To consume less data, some mobile users turn off images. They need the alt attribute to find out what the image is about.

`alt` also contributes to semantic meaning - it offers meaning to the image and suggests the purpose of the image content.

If the image is purely for presentation or decoration purposes, you should leave alt empty - `<img alt="">`. Assistive technology will then ignore this content.


#### Purpose of the image

You can use images for various reasons in your Web page like:

+ represent a concept, illustration or just a photograph that provide information
+ background for a button or link
+ display a quote or message in the form of text in an image
+ decorative images

Depending on the category the image fits into, the alt text differs. This W3C [WAI Images Tutorial](https://www.w3.org/WAI/tutorials/images/) is an excellent resource for deciding the category of your image and for learning how to write proper alt text for that category.

Here is an example of a tulip image using invalid source (that image is missing from the 'images' directory) and how it will look in a Web browser:

```html
<img src="image/tulips.png" alt="This is supposed to be an image of tulips">
```

[Example Code](src/2.4.2-ImgAlt.html)


#### Knowledge check 2.4.2

True or False? One of the functions of the 'alt' attribute is to provide information about the image to assistive technologies and search engines.

Ans: True<br/>
Explication: Search engines and assistive technology users do not see images and rely on the 'alt' attribute to find out what the image is about.


### Attributes: title, height & width

#### The 'title' Attribute

Try this: place your mouse on the image below. Don't click, just rest your cursor on it. 

<div style="display:flex;justify-content:center;align-items:center;flex-flow:row wrap;">
  <div><a href="https://courses.edx.org/courses/course-v1:W3Cx+HTML5.0x+1T2019/courseware/7e7a7ad104714c61b5b7bd35048b9ddc/3d0f9ea5b4ff4e59ba36c1bc1665e6f3/1?activate_block_id=block-v1%3AW3Cx%2BHTML5.0x%2B1T2019%2Btype%40vertical%2Bblock%4074262b9688b4439ebf7b5d934c231559">
    <img src="https://prod-edxapp.edx-cdn.org/assets/courseware/v1/64b9d57b8e2c1a03009b0cb79d5f8454/asset-v1:W3Cx+HTML5.0x+1T2019+type@asset+block/img-title.jpg" style="margin: 0.1em;" alt="Tulips in a basket" title="captTulips in woodburn tulip festival" width="250">
  </a></div>
</div>

Did you see the hidden message 'Tulips from woodburn tulip festival'? title is a global attribute we have seen before but worth mentioning again because it is very useful in an `<img>` tag. If you have a complicated image that could use a tooltip or description, you will want to use the `title` attribute.

```html
<img src="images/tulips.png" alt="This is supposed to be an image of tulips"
  title="Tulips from woodburn tulip festival">
```

The alt attribute is meant to be an alternate source of information while the title attribute should provide additional information about the image.

__Note__: For images, you __must__ use an `alt` attribute as there is no guarantee that the title attribute is presented to assistive technology users. The title attribute should not be relied upon for important information, and it should not be used in place of the alt attribute.


#### The 'height' & 'width' Attributes

Not all your images come in the right size for your Web page. The width and height attributes can be used to resize the image in pixels without using an external editor.

Here is my original image:

<div style="display:flex;justify-content:center;align-items:center;flex-flow:row wrap;">
  <div><a href="https://courses.edx.org/courses/course-v1:W3Cx+HTML5.0x+1T2019/courseware/7e7a7ad104714c61b5b7bd35048b9ddc/3d0f9ea5b4ff4e59ba36c1bc1665e6f3/1?activate_block_id=block-v1%3AW3Cx%2BHTML5.0x%2B1T2019%2Btype%40vertical%2Bblock%4074262b9688b4439ebf7b5d934c231559">
    <img src="https://prod-edxapp.edx-cdn.org/assets/courseware/v1/c92337ae06a2117b39c05568d1885b00/asset-v1:W3Cx+HTML5.0x+1T2019+type@asset+block/badgehtml5.png" style="margin: 0.1em;" alt="HTML5 logo not resized" title="Example image not resized">
  </a></div>
</div>

Clearly too big for the page. The original image dimensions is 345x523 in pixels. Pixel is short for picture element. These are the little dots that make up your image on a computer display like the monitor or laptop you are viewing this in. Pixels are generally too small to see (unless you look really close) and a screen might be made up of millions of pixels.

Now, if I want to resize the HTML logo above by half:

```html
<img src="images/html5.png" alt="HTML resized image" title="Resized image seems to fit the page better" 
  height="173" width="262">
```
<div style="display:flex;justify-content:center;align-items:center;flex-flow:row wrap;">
  <div><a href="https://courses.edx.org/courses/course-v1:W3Cx+HTML5.0x+1T2019/courseware/7e7a7ad104714c61b5b7bd35048b9ddc/3d0f9ea5b4ff4e59ba36c1bc1665e6f3/1?activate_block_id=block-v1%3AW3Cx%2BHTML5.0x%2B1T2019%2Btype%40vertical%2Bblock%4074262b9688b4439ebf7b5d934c231559">
    <img src="https://prod-edxapp.edx-cdn.org/assets/courseware/v1/c92337ae06a2117b39c05568d1885b00/asset-v1:W3Cx+HTML5.0x+1T2019+type@asset+block/badgehtml5.png" style="margin: 0.1em;" alt="HTML5 logo resized" title="Example image resized" height="173" width="262">
  </a></div>
</div>

Actually, you don't need to define both width and height. You can just specify either height or width and the aspect ratio will be adjusted. For example, the image above can be achieved using the following too:

```html
<img src="images/html5.png" alt="HTML resized image" 
  title="Resized image seems to fit the page better" height="173">
```

The use of these attributes really depends on how you are using the image. If it is part of an [image grid](https://www.imagely.com/wp-content/uploads/2013/03/adding-functionality-justified-image-grid-03.png) or a list with multiple images of the same size, it is best achieved by CSS. So you don't have to bother adding the same dimensions to every image and it will be repetitive. Plus it is generally bad practice to encode dimensions directly into the HTML.

However, if you are adding the image into some content and it needs to be a certain size for the visual flow of the reader, then it is best to add it to HTML using the `height` and `width` attributes. This is to avoid cluttering your CSS with a style for every image in your page. This is also useful if you are changing or removing the image: you can just remove it from your HTML and not deal with remembering to remove it from your CSS too.


#### Knowledge check 2.4.3

True or False? Setting the size for an image must always be done using the 'height' and 'width' attributes.

  Ans: False<br/>
  Explication: False. You can also use CSS to set height and width for an image. You are encouraged to use CSS when you have multiple images of the same size. If you have different sizes for every image as part of your content, you can add it using 'height' and 'width' attributes to avoid cluttering your CSS. Note that if you wish to maintain the aspect ratio of the image, specifying either height or width is sufficient.


### Decorative images

#### Should all images be part of HTML content?

A significant part of images on the Web are not used for any meaning. They merely serve a decorative purpose and fall under the presentation category. How do you identify these images? Well, if you have nothing relevant to put in your alt attribute or if you feel like it is not important to your or to the prospective reader, it should not be in your HTML.

We know we should keep content and style separate in HTML. Then how do we move these images out of content? Well, don't add them using the `<img>` tag in HTML. Use CSS instead. 

Examples of such images:

+ background images
+ fancy border graphics
+ banner graphics
+ pictures of landscapes or textures that are being used as elements behind or surrounding the content

Some pages (especially for video games, fancy magazines, etc) have a lot of eye-candy imagery that is not core to any of the semantic meaning of the page.

Can you identify these type of decorative images?

Find out from their tooltips!

<div style="display:flex;justify-content:center;align-items:center;flex-flow:row wrap;">
  <div><a href="https://courses.edx.org/courses/course-v1:W3Cx+HTML5.0x+1T2019/courseware/7e7a7ad104714c61b5b7bd35048b9ddc/3d0f9ea5b4ff4e59ba36c1bc1665e6f3/1?activate_block_id=block-v1%3AW3Cx%2BHTML5.0x%2B1T2019%2Btype%40vertical%2Bblock%4074262b9688b4439ebf7b5d934c231559">
    <img src="https://prod-edxapp.edx-cdn.org/assets/courseware/v1/74d84724ee496668618e246da1d6fcb2/asset-v1:W3Cx+HTML5.0x+1T2019+type@asset+block/image-background.jpg" style="margin: 0.1em;" alt="Beautiful landscape background image" title="Beautiful landscape background image" width="150">
    <img src="https://prod-edxapp.edx-cdn.org/assets/courseware/v1/e2fddb207225249526d2368fdac39457/asset-v1:W3Cx+HTML5.0x+1T2019+type@asset+block/image-texture.jpg" style="margin: 0.1em;" alt="Brick texture for use behind main content" title="Brick texture for use behind main content" width="150">
    <img src="https://prod-edxapp.edx-cdn.org/assets/courseware/v1/514eede426463409c5a59f946bbc89a6/asset-v1:W3Cx+HTML5.0x+1T2019+type@asset+block/image-border.jpg" style="margin: 0.1em;" alt="Fancy decorative border image" title="Fancy decorative border image" width="150">
    <img src="https://prod-edxapp.edx-cdn.org/assets/courseware/v1/f3eb43a6ef41d4bbd314f98bdbee1f26/asset-v1:W3Cx+HTML5.0x+1T2019+type@asset+block/image-banner.jpg" style="margin: 0.1em;" alt="Decorative banner graphic" title="Decorative banner graphic" width="150">
  </a></div>
</div>


#### Knowledge check 2.4.4

Suppose you have a small image that looks like a warning sign - ⚠.  You want to place it near a particular paragraph on your Web page. Should you use an  tag for the warning sign, or should you add it via CSS commands?

1. Image tag
2. CSS

  Ans: 1<br/>
  Explanation: A good way to decide which image should go into your content is to consider whether you want assistive technology or screen readers to understand the meaning of the image. In this case, a caution symbol might indicate some important text or warning and does not fall under the decorative images category. So, it should be added using the image tag in your content.


### Using 'img' tags

<video src="https://edx-video.net/W3CHTM502016-V015500_DTH.mp4" preload="none" loop="loop" controls="controls" style="margin-left: 2em;" muted="" poster="http://www.multipelife.com/wp-content/uploads/2016/08/video-converter-software.png" width="180">
  <track src="https://courses.edx.org/courses/course-v1:W3Cx+HTML5.0x+1T2019/xblock/block-v1:W3Cx+HTML5.0x+1T2019+type@video+block@7746cdf5eb2e446ab9313ae339857324/handler/transcript/download" kind="captions" srclang="en" label="English" default>
  Your browser does not support the HTML5 video element.
</video><br/>


### Activities - Images

1. Create a simple Web page that talks about your day using only text and images. Include at least three images and add the alt and title attributes.

  [My Code](src/2.4.6-ImagesQ1.html)

2. Look through the Web and your favorite Web sites and identify those that you think use a lot of decorative images.

  Check [Stack Overflow](https://stackoverflow.com/questions/20639180/explanation-of-how-nested-list-comprehension-works)

  + top-left corner: website logo
  + top-right corner: widgets of incoming box, new achievement, list of stack exchange sites
  + Ask Question widget
  + user icons for posters

3. Create a HTML page and add the following types of images:

  + Informative image that represents concepts and information
  + Decorative image
  + Images of text

  [Example code](src/2.4.6-ImagesQ3.html)

Use the `alt` attribute to provide alternate text for the images above.

Refer to the [WAI Images Tutorial](https://www.w3.org/WAI/tutorials/images/) for a guide to writing alternate text.

__Note__: If you wish to share your HTML code in the discussions, you can paste your code directly in a discussion forum post (highlight code and Ctrl+K/use the code widget) or use one of the following online code editors:

+ JS Bin: http://jsbin.com ([JS Bin tutorial](http://code.tutsplus.com/tutorials/javascript-tools-of-the-trade-jsbin--net-36843))
+ CodePen: http://codepen.io ([CodePen tutorial](https://css-tricks.com/video-screencasts/112-using-codepen/))

These are HTML, CSS, and JavaScript code editors that preview/showcase your code bits in your browser. It helps with cross-device testing, realtime remote pair programming.



## 2.5 Hyperlinks

### Introduction to hyperlinks

#### What Are Hyperlinks?

In a typical Web page, I am sure you have seen a sentences like these:

&nbsp;&nbsp;&nbsp;&nbsp;[Find out more](https://en.wikipedia.org/wiki/Hyperlink) about our offers!

Or something like this:

<p style="padding-left: 30px;"><a href="https://en.wikipedia.org/wiki/Hyperlink" target="_blank"><img alt="Buy now button for illustrating hyperlinks" src="https://prod-edxapp.edx-cdn.org/assets/courseware/v1/0573c0ed603120bf053860bb0d2a2314/asset-v1:W3Cx+HTML5.0x+1T2019+type@asset+block/buy-now.PNG" type="saveimage" target="[object Object]" width="231" height="44"></a></p>


Try clicking the blue text or the 'Buy Now!' button, if you haven't already (make sure to navigate back to the course).

Hyperlink is any text or image you can click and it will take you to another page. This page can be:

+ another Web page: e.g. the hyperlinks wiki page at `https://en.wikipedia.org/wiki/Hyperlink`
+ a bookmark (a specific part of a Web page): e.g. the History section of the Hyperlinks wiki page at `https://en.wikipedia.org/wiki/Hyperlink#History`

  We learned about using the id attribute as a link target in the unit about attributes earlier. If you have a section in your page, you can link to that section using the value of its `id` attribute (i.e. History) preceded by the number sign - #History

+ a local link (link to another part of the same Web page): e.g. `a_tag.asp` is a page that belongs to this Web site
+ an email: e.g. `mailto:helloauthor@w3c.com`


#### Why you should use text over image links

When it comes to hyperlinks, try to use text instead of images when possible.

+ Images are not as well understood or recognized as text.
+ Text is better for accessibility.
+ If you have text in an image like the 'Buy now' button, search engines do not recognize text in images.


#### Best Practices

+ Apply hyperlinks to short phrases. It is unusual to see the link tag used around a whole paragraph.
+ Make link phrase meaningful. Avoid phrases like 'Click Here' or 'Read More'. 'Click here to get help' is redundant when you can create a link around the phrase 'Get Help'. The link is an indication that it should be clicked.
+ Don't use short link text. It is easy to miss the 'blue' hyperlink if it is used on one word or character and is hard for users to click using touch screen.
+ Appearance - links have a default appearance in most browsers, blue and underlined. Ensure no other text in your page is underlined so as to avoid confusing the user. They might get frustrated trying to click text that they think is a link.
+ If you choose to have image links, it should have __alternate text__ that describes the purpose of the link instead of the image used - describe the target link.

```html
<a href="https://www.table-header-cells.com">
  <img src="table-th.png" alt="Introduction to table header cells and their usage">
</a>
```


#### Anchor Element

The hyperlink tag in html is simply `<a>`, and it is called the __anchor element__. Here is how it is used:

```html
<a href="https://en.wikipedia.org/wiki/Hyperlink">Click here</a> to go to the Wikipedia Hyperlink page.
```

Result: <strong>[Click here](https://en.wikipedia.org/wiki/Hyperlink) to go to the Wikipedia Hyperlink page.</strong>

Note: The anchor element should not be confused with the <link> tag. The `<link>` tag is used to define a link between a document and an external resource like an external style sheet. You will learn more about the <link> tag in the next chapter.

##### States of a hyperlink:

If the link has not been clicked, it will be blue and underlined. Now, click on the link and you will see that a visited link looks purple and underlined. Apart from unvisited and visited links, there is also a status called active link. A link becomes active while the user is clicking on it. During this time, the link will be red and underlined.

1. __Unvisited__: blue + underlined
2. __Visited__: purple + underlined
3. __Active__: red + underlined


#### Usage

The `<a>` tag can surround text or an image. 

```html
<!-- Text in a hyperlink-->
<a href="https://www.qwant.com/">If you click on me, I will take you to qwant.com</a>
<!-- Paragraph in a hyperlink-->
<a href="https://www.qwant.com/"><p>If you click on me, I will take you to qwant.com</p></a>
<!-- Image in a hyperlink-->
<a href="https://www.qwant.com/"><img src="images/qwant-image.png" alt="Image navigating to Qwant"></a>
```

You can even use the anchor element to add your email address under the contacts section of your Web page.

```html
<p>Feedback: <a href="mailto:authors@example.com">Send Mail to Authors</a></p>
```

Result (try the hyperlink below):

Feedback: [Send Mail to Authors](authors@example.com)

You can add a subject to the email.

```html
<p>Feedback: <a href="mailto:authors@example.com?Subject=Hello">Send Mail to Authors with Subject</a></p>
```

Result (try the hyperlink below)

Feedback: [Send Mail to Authors with Subject](authors@example.com)

Nevertheless, you should probably avoid using hyperlinks for email addresses:

+ The email address usually opens up on the default email client on the user's computer which they might not use. This defeats the whole purpose.
+ Providing your email address in your Web page directly as text or a hyperlink will expose your email address. Bots or spam crawlers can be used to search the Web to pick up email addresses for spam. You should avoid this if possible and use contact forms instead.


#### Knowledge check 2.5.1

True or False? The anchor element is the same as the `<link>` tag.

  Ans: False<br/>
  Explication: They are not the same. The anchor element is used for hyperlinks while the `<link>` tag is used to define a link between a document and an external resource like an external style sheet.


### Attributes: href and target

#### The 'href' attribute

The only attribute we have seen thus far in this chapter of hyperlinks is `href`.

`href` points to the URL that the link should jump to. Though it is an optional attribute, without it, the `<a>` tag will not be a hyperlink because it obviously has no idea where to jump to.

The `href` attribute takes a URL. This URL can be in the form of:

+ a link to an external Web site also known as [absolute URL](http://www.differencebetween.com/difference-between-an-absolute-and-vs-a-relative-url/).

  ```html
  <a href="https://qwant.com"></a>
  ```

+ a link to a file or page within the same Web site also known as [relative URL](http://www.differencebetween.com/difference-between-an-absolute-and-vs-a-relative-url/).

  ```html
  <a href="contacts.html"></a>
  ```

+ a link to an element on the same page. The element, is referenced using its ID. E.g. If you want to link to a div with id='details', the corresponding anchor tag will be:

  ```html
  <a href="#details"></a>
  ```

+ protocols such as:
  + mailto: | for email addresses. 

  ```html
  <a href="mailto:abc@alphabets.com"></a>
  ```

#### The 'target' attribute

target specifies the destination where the linked URL in href should be opened. It can take a variety of different values, but for our purposes we'll focus on the two below.

<table style="font-family: arial,helvetica,sans-serif; table-layout: auto;" cellspacing="0" cellpadding="5" border="1" align="center">
<tbody>
  <tr>
    <td style="background-color: #3d64ff; color: #ffffff;" width="40%">Destination</td>
    <td style="background-color: #3d64ff; color: #ffffff;" width="10%">Attribute value</td>
    <td style="background-color: #3d64ff; color: #ffffff;" width="30%">Example</td>
    <td style="background-color: #3d64ff; color: #ffffff;" width="15%">Result (try this)</td>
  </tr>
  <tr>
    <td>In the same view where the link resides. If no target is specified, this is the default behavior.</td>
    <td>_self</td>
    <td>&lt;a href="<span style="color: #339966;">https://qwant.com/</span>" target="<span style="color: #339966;">_self</span>"&gt;&lt;/a&gt;</td>
    <td><a href="https://qwant.com/" target="_self">LINK will open in same window</a>&nbsp;(Navigate back to the course by clicking Back button in browser)</td>
  </tr>
  <tr>
    <td>
      <p>In a new window or tab. This is very convenient if you want to link the user to a Web page without having the current page disappear. By clicking on the previous  window or tab, they can redirect to the page where the link is.</p>
      <p><strong>Note: </strong>It is best to inform users that the page will open in a new tab or window when using '_blank' as some may not be aware of the new tab having  opened.</p>
    </td>
    <td>_blank</td>
    <td>&lt;a href="<span style="color: #339966;">https://qwant.com/</span>" target="<span style="color: #339966;">_blank</span>"&gt;&lt;/a&gt;</td>
    <td><a href="https://qwant.com/" target="_blank">LINK will open in new window</a></td>
  </tr>
</tbody>
</table>


#### Knowledge check 2.5.2

True or False? The 'mailto:' protocol in the `href` attribute can validate the email address provided.

  Ans: False, xTrue<br/>
  Explication: It will only open an email client adding the address provided in the recepient's list. It does not have the capacity to check the validity of the email address.


### Attributes: media and download

#### The 'media' attribute

The media attribute was introduced in HTML5. We will look at it briefly here. It is used to specify what kind of media or device the URL you linked to in href is optimized for. The URL could be targeted for special devices like projectors, speech synthesizers or pages meant to be printed. It is useful if you want to cater your target document that the URL points to a particular device type.

Imagine you have a page scattered with multiple images and you want to display this page on a handheld device. Handheld devices are known to have small screens and limited bandwidth. We want to align the page better for a small screen and reduce the size of images. So the media attribute allows us to tell the anchor element that this page is targeted for handheld devices. You do this by providing a value for the attribute. This value could be any valid [media query](http://www.w3.org/TR/css3-mediaqueries/) and is a combination of __device type__ and __media rendering values__.

Let's look at another example - you could create a print link to a long content heavy page that will redirect you to a print version of the same. You want this print version to be formatted into one page ideal for printing and with resolution of 250 dpi. Here is how the HTML5 code will look like:

```html
<a href="https://en.wikipedia.org/wiki/Media_queries?output=print" 
  media="print and (resolution:250dpi)">Print wiki page about media queries</a>
```


#### The 'download' attribute

The download attribute is also new in HTML5 and it makes a link download a file instead of navigate to another location. It takes in the filename as value but the value is optional. So the download attribute can be specified in the following ways:

```html
<a href="/assets/hello.txt" download>
<a href="/assets/hello.txt" download="new-name-for-text-file">
```

If you do not specify a value for download, it will download the file with name unchanged. Else it will download the file with file name modified according to value specified.

```html
<a href="/assets/hello.txt" download>
```

... will download the file with the same name - 'hello.txt'.

```html
<a href="/assets/hello.txt" download="new-name-for-text-file">
```

... will download the file after altering its name to - 'new-name-for-text-file.txt'.

Example (try the hyperlink below in Google Chrome):

[Click to Download](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/6e709b3765de6510e212932331a0bf52/asset-v1:W3Cx+HTML5.0x+1T2019+type@asset+block/hello.txt)

__Note__: download attribute will only works on Chrome, Firefox and Opera. It is [not supported in all browsers](http://caniuse.com/#search=download). Try the download attribute in a html file of your own and run it in different browsers to see how it behaves.

#### Knowledge check 2.5.3

True or False? The extension of the file name is not needed for 'download' attribute's value.

  Ans: true, xFalse<br/>
  Explication: The value should be the new name of the file downloaded. The extension is not needed but providing it is alright. Try both scenarios to find out how the browser responds.


### Use of hyperlink attributes

<video src="https://edx-video.net/W3CHTM502016-V013500_DTH.mp4" preload="none" loop="loop" controls="controls" style="margin-left: 2em;" muted="" poster="http://www.multipelife.com/wp-content/uploads/2016/08/video-converter-software.png" width=180>
  <track src="https://courses.edx.org/courses/course-v1:W3Cx+HTML5.0x+1T2019/xblock/block-v1:W3Cx+HTML5.0x+1T2019+type@video+block@a139001a69544fd081045c81fdfc8bc8/handler/transcript/download" kind="captions" srclang="en" label="English" default>
  Your browser does not support the HTML5 video element.
</video><br/>

[Example code: Page 1](src/2.5.5-Hyperlink1.html)


### Activities - Hyperlinks

1. Test the anchor element by providing broken or invalid links. How does the browser respond?

  [Example code](src/2.5.6-HyperlinksQ1.html)

2. Create a simple 'Contact me' page and include the following using hyperlinks where possible:

  + Short introduction (not more than three lines) about yourself
  + Social media information
  + Email

  In the same page, add navigation at the start for parts of your page like Introduction, Social Media and Email. Use hyperlinks and the 'id' attribute to link to each section from nav.

  [Example code](src/2.5.6-HyperlinksQ2.html)

3. Create an HTML page with a link that utilizes the download attribute. Try your code in Internet Explorer and Google Chrome. What is the difference in behavior that you see? Why is this happening?

  All the browsers, Chrome, IE and Edge, are open the text and graph files instead of showing download instruction.  

  [Example code](src/2.5.6-HyperlinksQ3.html)

4. Can you think of different scenarios where you would use target values '_self' and '_blank'?

Note: If you wish to share your HTML code in the discussions, you can paste your code directly in a discussion forum post (highlight code and Ctrl+K/use the code widget) or use one of the following online code editors:

+ JS Bin: http://jsbin.com ([JS Bin tutorial](http://code.tutsplus.com/tutorials/javascript-tools-of-the-trade-jsbin--net-36843))
+ CodePen: http://codepen.io ([CodePen tutorial](https://css-tricks.com/video-screencasts/112-using-codepen/))

These are HTML, CSS, and JavaScript code editors that preview/showcase your code bits in your browser. It helps with cross-device testing, realtime remote pair programming.


### Recipe project - Module 2

We are now going to continue building on the recipe project we started in Module 1.  You can find our version in the [CodePen](https://codepen.io/w3devcampus/pen/pPaPXZ) [here](src/2.5.7-ProjectSample.html).

__Feel free to build on your own or on that one, whichever you prefer.__  We can apply some of what we've learned this week to improve our page, both in terms of looks a structure.  Also, we've added a couple more recipes, so we have a more realistic situation, i.e. multiple recipes rather than just one.

Try to make good use of semantic elements, images and hash links to get something like [this](src/2.5.7-ProjectSample2.html)

[My Project Code](src/2.5.7-Recipe.html)


#### Live coding video: recipe project - Module 2

<video src="https://edx-video.net/W3CHTM502016-V008500_DTH.mp4" preload="none" loop="loop" controls="controls" style="margin-left: 2em;" muted="" poster="http://www.multipelife.com/wp-content/uploads/2016/08/video-converter-software.png" width=180>
  <track src="https://courses.edx.org/courses/course-v1:W3Cx+HTML5.0x+1T2019/xblock/block-v1:W3Cx+HTML5.0x+1T2019+type@video+block@2e778a901b284527aacc589062ead4c7/handler/transcript/download" kind="captions" srclang="en" label="English" default>
  Your browser does not support the HTML5 video element.
</video><br/>


## 2.6 Exercises - Module 2


### Attributes (1-9)

1. Hey you!

  ```html
  <!DOCTYPE html>
  <html>
    <meta charset='UTF-8'>
    <head>
      <p> HEY YOU </p>
      <style>
      </style>
      <script>
      </script>
    </head>
    <body>
      <h1>YO</h1>
    </body>
  </html>
  ```

  Is it valid to have a paragraph element inside the `<head>` tag like in the code above? (If you are unsure, please check the W3C cheatsheet or MDN’s `<head>` element page)

  Ans: No <br/>
  Explanation: You cannot have a paragraph element inside `<head>`. Elements that can be used inside `<head>` are `<title>`, `<base>`, `<link>`, `<style>`, `<meta>`, `<script>` and `<noscript>`.


2. Show me your id

  ```html
  <p id="intro">Hi! My name is Alex and I love to cook.</p>
  ```

  Unlike most attributes, the id of an element should be:

  1. split by spaces if you want to specify multiple values
  2. the same across a given type of element i.e. all paragraphs have the same id
  3. unique to that element and can only be used once
  4. written in all caps (“ID=“)

  Ans: 3 <br/>
  Explanation: The id of an element should be unique and can only be used once. Unlike the class attribute, you cannot have more than one id value for an element.


3. Tag specific?

  True or False? The non-global attribute ‘size’ can only be applied to one tag.

  Ans: False <br/>
  Explication: Non-global attributes can apply to more than one tag. The size attribute can be applied to `<input>` and `<select>` tags. Read more about them in the HTML attribute reference available at Mozilla Developer Network.


4. It's required!

  What are the required attributes in an image tag? (Select all that apply - 2 answers are correct!)

  1. src
  2. title
  3. height
  4. alt

  Ans: 14  <br/>
  Explanation: The only two required attributes of an image tag are src and alt. All others are optional. src is used to specify the location the image should be fetched from and alt provides a short description of the image that is displayed for assistive technology users, search engines or if the image does not display.


5. Tooltip in title

  True or False? A tooltip in the title attribute can only be used on images.

  Ans: False <br/>
  Explication: Title is a global attribute and so can be used on any element. Another good usage is to expand abbrievations. `<abbr title="HyperText Markup Language">HTML</abbr>`


6. Browser support?

  True or False? All browsers support all attributes.

  Ans: False <br/>
  Explication: Not all browsers support all attributes. http://caniuse.com is a good resource to find out browser support for a particular attribute. Here is an example for the [download attribute](http://caniuse.com/#search=download%20attribute).


7. Valid id attribute?

  Which of the following is a valid value following best practice for the id attribute?

  1. `<p id=""> </p>`
  2. `<p id="NaViGaTiOn"> </p>`
  3. `<p id="score-display"> </p>`
  4. `<p id="Frequently asked questions"> </p >`

  Ans: 3 <br/>
  Explanation:
  + Frequently asked questions: it hould not contain spaces
  + NaViGaTiOn: it does not follow best pratice, as you are advised not to mix cases.
  + score-display: it follows all naming rules
  + "": the value must be of at least one character


8. Truly global

  Which of the following statements about global attributes is true?

  1. All global attributes are of type boolean
  2. Global attributes are common to all elements
  3. Only 'id' and 'class' are global attributes
  4. Global attributes only apply to elements that do not have any attributes of their own

  Ans: 2 <br/>
  Explanation: Global attributes are a list of attributes that are common to all elements in HTML.


9. Multiple classes

  What do you use to split multiple classnames in the 'class' attributes?

  1. You can only specify one classname in the 'class' attribute
  2. space
  3. comma
  4. colon

  Ans: 2 <br/>
  Explanation: You can include two classnames for an element by separating them by space.<br/>
  `<p class="poetry shakespeare">Insert Shakespeare poetry here</p>` <br/>
  The paragraph above has two classnames - poetry and shakespeare, split by space.


### Semantic elements (10-16)


10. Semantic elements

    True or False? Semantic elements, like article and section, don't use attributes.

    Ans: False <br/>
    Explanation: Though semantic elements may not need an attribute to indicate its semantics, they can still use global attributes that apply to all elements


11. My text is important!

    Which tag will you use to convey importance in your text?

    a. Emphasis `<em>`
    b. Strong `<strong>`
    c.Italics `<i>`
    d. Bold `<b>`

    Ans: 2 <br/>
    Explanation: The strong element represents strong importance, seriousness, or urgency for its contents while emphasis is used to stress emphasis of its contents.

12. Mark my words

    a. What is the purpose of the semantic element `<mark>`?
    b. so it can be refered to by other semantic elements
    c. underline text
    d. strikethrough text

    Ans: 4 <br/>
    Explanation: `<mark>` is used to highlight text. It will display with a yellow background in most browsers.


13. Non-semantic tags

    Which of the following is a non-semantic tag?

    a. `<body>`
    b. `<img>`
    c. `<div>`
    d. `<p>`

    Ans: 3 <br/>
    Explanation: Semantic elements suggest the content within tags. The `<div>` tag does not provide any information of the content within.


14. header and footer elements

    True or False? You can have multiple header and footer elements in your Web page.

    Ans: True <br/>
    Explication: `<header>` and `<footer>` elements do what it is intended to for its parent element which can be a section. So each section in your Web page can have a header and footer just like each article, div, etc.


15. Who does semantic elements benefit?

    Who does semantic elements benefit? (select all that apply - 4 correct answers!)

    1. You
    2. Assistive technology users
    3. The browser
    4. The search engine
    5. The server

    Ans: 1234 <br/>
    Explanation: Semantic elements convey more information about your HTML document's content and structure which is going to be useful for you when you revisit your code after a long break. For the browser, it can better differentiate different types of data which results in better display of content in different devices. Assistive technology like screen readers gather more information from semantic HTML. It will read content marked up with `<em>` with emphasis or read header tags in a higher voice to indicate it is a heading. Better markup structure imrpoves the automated processing of documents in search engines.



16. Room with a view

  Which semantic element has content that should be expanded to view?

  1. figcaption
  2. details
  3. expand
  4. summary

  Ans: 2<br/>
  Explanation: The details element contains `<summary>` and other content. Only `summary` will be displayed and it should be expanded to view all other content.


### Images (17-24)

17. Image info

  Which attribute do you use when you want to provide more information about a complicated image?

  1. alt
  2. info
  3. src
  4. id
  5. title

  Ans: 5 <br/>
  Explanation: Title attribute creates a tooltip with additional information when you hover the mouse over the image. This should not be confused with the alt attribute which is a source of alternate information for the image.


18. Best image path

  Which of the following image paths follow the best practice for a relative URL?

  1. package\assets\Images\example.PNG
  2. images/example.png
  3. Package/Assets/Images/Example.png
  4. images\example.png

  Ans: 2 <br/>
  Explanation: An image path should use the unix path name separator (/). For any path relative to the file, the simplest is to always keep the images directory at the same level, or one level down. The recommended practice is to use lower case for all directories, file names and file extensions because mixed case is prone to cause mismatched capitalization (directory name is 'Images' but your path uses 'images') which doesn't always work.


19. Half image

  True or False? You need to use both height and width attributes to shrink your image by half.

  Ans: False <br/>
  Explication: Specifying either one is sufficient and the aspect ratio will be maintained.


20. Adding images

  True or False? Images can be added to your Web page in more than one way.

  Ans: True <br/>
  Explication: Other than the image tag, they can also be added through CSS which is the recommended way to add images that serve a decorative purpose.


21. Closing tag

  True or False? The closing tag for image is `</img>`.

  Ans: False  <br/>
  Explanation: The image tag has no closing tag.


22. What does the 'alt' attribute do?

  What does the 'alt' attribute do?

  1. used to distinguish image and text links by a screen reader
  2. describes the information the image conveys or its function
  1. display information about an ambiguous image as a tooltip
  4. links to a URL

  Ans: 2 <br/>
  Explanation: The 'alt' attribute is used to provide a short description of the image or the function it serves for users who use assistive technology like screen readers, for search engines or if the image cannot be displayed for some reason. For a longer description, either add a link to the description after the image, describe the location of the longer description in the alt attribute, or use figure to structurally associate the image with its longer description.


23. Background image

  If you have an image you want to add as a background to your Web page, your 'alt' attribute's value should be:

  1. no alt attribute is needed
  2. empty - ""
  3. a background image
  4. a decorative image

  Ans: b <br/>
  Explanation: Images used for decoration or presentation purposes should have an empty value for alt. `<img alt="">`


24. Give me an alt!

  Which of the following is a good alt attribute value for the following image: [alt attribute image](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/b6a326d9198fb5b5d72a7a7205537a05/asset-v1:W3Cx+HTML5.0x+2T2018+type@asset+block/surprise.jpg)?

  1. Image 3
  2. Boy looking at his school computer overjoyed and surprised by his exam results
  3. Surprised boy
  4. "" - no value

  Ans: 2 <br/>
  Explanation: This looks like an informational image so some text that describes the information displayed visually is appropriate. <br/>
  Empty alt value is typically used for decorative images.



### Hyperlinks (25-28)


25. Download attribute:

  What is the purpose of your download attribute's value in a hyperlink?

  1. It is a boolean value authorizing download
  2. It is the name of file in the location specified in href
  3. Downloaded file name will be modified according to value specified
  4. Download attribute has no value

  Ans: 3 <br/>
  Explanation: The download attribute can have a value. If no value is specified, it downloads the file preserving the original file name. If a value is provided, it modifies the file name according to the value specified when downloading.


26. Linking documents:

  Different documents can be linked together using which one of these elements?

  1. href
  2. src
  3. hyperlink
  4. anchor

  Ans: 4 <br/>
  Explanation: The anchor element is used to link different documents across the internet. There is no element called 'hyperlink'. 'src' and 'href' are attributes.


27. Anchor element:

  True or False? The anchor element is only used to link from one page to another.

  Ans: False <br/>
  Explication: While navigating to another page or part of your page is the typical use for an anchor element, the use of the download attribute introduced in HTML5 makes a link download a file instead of navigate to another location.


28. Hyperlink destination

  ```html
  <a href="https://w3.org" target="_blank">W3C</a>
  ```

  What does the code above do?

  1. Opens the page in a separate frame
  2. Opens the page in a new tab or window
  3. Doesn't do anything as the code above is invalid
  4. Opens the page in the same tab or window

  Ans: b <br/>
  Explanation: target value '_blank' will open in a new tab/window while '_self' opens in the same tab/window.





