# System 1 - Foundations I

## **Advanced CSS**

## CSS Specificity

### Cascading Style Sheets (CSS)

- The *cascade* is an algorithm that tells us how to combine, prioritize, and override CSS properties based on their source
- **General Specificity**: selectors are broken down into three levels of specificity
  - Element selectors, such as `h1`
    - Lowest specificity
    - Talks about very *general* elements
  - Class selectors, such as `.my-heading`
    - Medium specificity
    - Talks about a subset of elements that the user defines
  - ID selectors, such as `#main-title`
    - Highest specificity
    - Talks about one element only
    - This is why IDs **must** be unique

### Complex Selectors

> Check out this [MDN Reference](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors) on CSS selectors.

**Multiple Selectors**: Used when selecting elements that exhibit more than one trait, selectors are placed together

**Grouped Selectors**: Used to apply the same CSS rule to several elements

- Use a comma `,` to group different selectors together
- We can group an unlimited number of selectors together
- *Multiple* selectors and *Grouped* selectors are NOT the same
- Multiple selectors represent an **and** relationship
- Grouped selectors represent an **or** relationship

**Child Selectors**: Used to control the depth that our descendant rule reaches

- Child selectors target only the children of the given element
- Can group child selectors to select further descendants

***

## CSS Units

CSS Units refer to the possible units of measurement for CSS properties:

- px
- cm, inches, mm
- em, rem
- %
- vh, vw

### Absolute Units

The absolute length units are fixed in relation to each other and anchored to some physical measurement. They are mainly useful when the output environment is unknown.

- **px (pixels)**: Widely used and a holdover from the early days of the internet
- **cm, inches, mm**: Rarely used and meant for print layouts

**Pixels**: CSS pixels are not pixel perfect. Can be used for padding, borders, shadows, etc.

- Device Pixel: A single physical point on a device display
- CSS Pixel (Optical Reference Pixel): ~0.26mm

The better the resolution the smaller the pixel. A retina display may have have 2x pixels in a given area.

**The Problem**:

- As our devices evolve, so must our web development practices.
- With the advent of Retina devices and smartphones: `1px (desktop) =/= 1px (smartphone)`

### Relative Units

Relative length units specify a length relative to another length. Style sheets that use relative units can more easily scale from one output environment to another. E.g. can more easily scale from a mobile screen to a desktop monitor.

- **% (percentage)**: Relative to containing block or parent element. Used for layouts in responsive design. Containing block needs to have a value set, great for defining widths.
- **em, rem**: Relative to font size of current element. Relative to root font size. Preferable to use for padding, margin, and *font size*. *rem* is newer than *em* and is recommended. Good for typography.
- **vh, vw**: Relative to 1% of viewport height or width. Good for full viewport banners.
- **vmin**: Relative to 1% of the viewpoint smallest side.
- **vmax**: Relative to 1% of the viewport largest side.

## Exercises

### Exercise 6: Box Model

Test understanding of the box model and ability to use CSS to manipulate an element's box model regions.

**Question 1**
width: 200px;
height: 200px;
padding: 35px 0px 0px 0px; (padding-top: 35px;)
margin: 32px;
border-width: 1px;

**Question 2**
width: 400px;
height: 255px;
padding: 0px 25px;
margin: 10px 15px 50px 25px;
border-top: 35px;
border-bottom: 32px;

**Question 3**
width: 100px;
height: 333px;
padding: 45px 0px;
margin: 0px 20px 10px 25px;
border-left: 5px;
border-right: 5px;

**Question4**
width: 900px;
height: 100px;
padding: 15px 10px 51px 15px
margin: 100px 15px 5px 5px
border-right: 5px;
border-bottom: 10px;
border-left: 5px;

**Question 5**
width: 650px;
height: 1050px;
padding: 10px
margin: 0 15px 5px 5px;
border-top: 25px;
border-right: 5px;
border-bottom: 15px;
border-left: 5px;

## Lecture: Display

### display: `block`

- Starts on its own "row" or "line"
- `display: block` takes up ALL available width on the page. Greedy w/width & Conservative w/height
- Elements are are *block* by default: `body`, `p`, and `div`

### display: `inline`

- Often used for text/paragraphs
- Able to wrap content in a paragraph without breaking the flow of text.
- Takes up only the width & height needed to fit the content
- Elements that are *inline* by default: `span` and `a`
- Example usage: Changing the color or text style of one word in a paragraph

### display: `inline-block`

- A combination of `inline` and `block`
- Allows us to define margins, height, etc.
- Takes up ONLY the width needed
- Act as *inline-block* by default: `img` and `button`
- Useful when not concerned about breaking the flow of text (ie. not a paragraph or sentence)

### Hiding and Showing Elements

- `display: none`
  - Removes the item from the visual flow of the document
  - Great for hiding things

- `visibility: hidden`
  - Also hides elements
  - Keeps the occupied space empty

- Both have a negative effects on assistive screen devices, like screen readers

### Document Layout

### SVG: Scalable Vector Graphics

- Vector instructions sent to your computer which will begin to draw a simple image based on coordinates/vectors. Similar to connect-the-dot or drawing a graph.
- An XML-based vector image format for defining two-dimensional graphics, having support for interactivity and animation. The SVG specification is an open standard developed by the World Wide Web Consortium since 1999.

### Tips & Tricks

- `text-align: center` only applies to `inline` or `inline-block` display elements
