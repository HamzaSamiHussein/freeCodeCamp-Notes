# freeCodeCamp Notes

These notes is from what i see i important on each topic in freeCodeCamp course.

<a href="#lastNote">Last note</a>
<small> - This link works in the link mentioned in about section **only**</small>

___

## BASIC HTML AND HTML5 TOPIC:-

Link to Internal Sections of a Page with Anchor Elements:-

```html
<a href="#contacts-header">Contacts</a>


<h2 id="contacts-header">Contacts</h2>

```

___

## BASIC CSS TOPIC:-

-z-index

-[css positioning](https://www.youtube.com/watch?v=jx5jmI0UlXU)

-hsl() -> hus, saturation, lightness

-rgba ->red, green, blue, alpha

-Create a Gradual CSS Linear Gradient:- background: linear-gradient(90deg, color1, color2, color3, .....)

-background:- repeating-linear-gradient(45deg, yellow 0px, yellow 40px, black 40px, black 80px);

___

-Transform scale Property to Change the Size of an Element:-

```css
p {
    transform: scale(2);
}
```

___

-The next function of the transform property is skewX(), which skews the selected element along its X (horizontal) axis by a given degree.

```css
p {
    transform: skewX(-32deg);
}
```

___

-Use transparent to hide the color of something ->

```css
background-color: blue;  --> background-color: transparent
border-radius: 0px;
box-shadow: 25px 10px 10px 10px green;
```

___

-(div::before and div::after) :- These pseudo-elements are used to add something before or after a selected element.
<https://www.youtube.com/watch?v=pGrfemW4dcY>

___

-How the CSS @keyframes and animation Properties Work:-
  Example:-

```css
   #anim {
       animation-name: colorful;
     animation-duration: 3s;
    }
```

```css
   @keyframes colorful {
      0% {
  background-color: blue;
     }
      100% {
        background-color: yellow;
      }
   }
```

___

-animation-fill-mode: forwards; --> when the duration finish the 500ms we want to still the hover highlighter we can do it by ((animation-fill-mode: forwards;))

```css
  button:hover {
    animation-name: background-color;
    animation-duration: 500ms;
    animation-fill-mode: forwards;
  }
```

```css
  @keyframes background-color {
    100% {
      background-color: #4791d0;
    }
  }
```

-@keyframes like the download when it reaches the 50% do the code block inside it, when it reaches the 1% do the code clock inside it.

-animation-iteration-count:infinite;

- Change timing animation:- <animation-timing-function: (ease, ease-in, ease-out, linear).

```css
 #ball1 {
  left:27%;
  animation-timing-function: linear;
 }
```

___

-animation-duration: 2s;

___

-<https://cubic-bezier.com/>

___

## TOPIC:- APPLIED ACCESSIBILITY FOR USERS WHO ARE USING *ASSISTIVE TECHNOLOGIES* USING HTML SEMANTIC:-

-when to use article and section tag
<https://www.youtube.com/watch?v=Eyndz5R-Vkg>

___

-Add audio tags ->ex->

```html
 <audio id="audioClip" controls>
  <source src="www.s3.com/route.mp3" type="audio/mpeg" />
 </audio>
 ```

___

 -Use label for input in form tag ->ex->

```html
<form>
     <label for="email" >Email:</label>
      <input type="text" id="email" name="email">
</form>
```

___

-Since ```<radio>``` buttons often come in a group where the user must choose one, there's a way to semantically show the choices are part of a set.
The ```<fieldset>``` tag surrounds the entire grouping of radio buttons to achieve this. It often uses a ```<legend>``` tag to provide a description for the grouping, which is read by screen readers for each choice in the ```<fieldset>``` element. ->ex->

```html
<form>
  <fieldset>
    <legend>Choose one of these three items:</legend>
    <input id="one" type="radio" name="items" value="one">
    <label for="one">Choice One</label><br>
    <input id="two" type="radio" name="items" value="two">
    <label for="two">Choice Two</label><br>
    <input id="three" type="radio" name="items" value="three">
    <label for="three">Choice Three</label>
  </fieldset>
</form>
```

___

-Time tag has datetime attribute which  accessed by assistive devices.
It helps avoid confusion by stating a standardized version of a time, even if it's written in an informal or colloquial manner in the text.
->ex->

```html
<time datetime="2013-02-13">
last Wednesday</time>
```

___

-If you have chart and you want to make screen-reader read your chart make it table, but you have to remove the table from your document and make it hidden from the users and only accessible from the screen-reader. ->ex->
(this class put it on the table tag)

```css
  .sr-only {
    position: absolute;
    left: -10000px;
    width: 1px;
    height: 1px;
    top: auto;
    overflow: hidden;
  }`
```

___

-Screen reader users have different options for what type of content their device reads.
This includes :-
1. skipping to (or over) landmark elements. 
2. jumping to the main content. 
3. getting a page summary from the headings. 
4. Another option is to only hear the links available on a page.by reading the link text, or what's between the anchor (a).

__

-Use accesskey for buttons "a" tag to make keyboard-users click these links.

```html
<a accesskey="g">google</a>
<button accesskey="f">facebook</button>
```

___

-tabIndex="0,+1,-1", use it in HTML elements to make it important whn users use keyboard navigate through page, use p:focus{} to make  a CSS style when the use focus on the selected element ->ex.->

```html
<p tabindex="0" >Hamza</p>
```

___


-use tabindex="1,2,3,etc.." to Specify the Order of Keyboard Focus for Several Elements.

___
<small id="lastNote"> Last note </small>

## RESPONSIVE WEB DESIGN PRINCIPLES TOPIC:-
