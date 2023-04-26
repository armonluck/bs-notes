# System 2 - Foundations II

## BS Lecture: Positioning + Float `02/14/23`

***

### Sass - Syntactically Awesome Style Sheets

- Make sure to click “Watch Sass” when working on a .scss file. **"Watch Sass"** will show you any errors that are in your code as you save

### CSS Positioning

- Developers often need elements to move outside of their normal position
- Display property does NOT allow control over the exact position of an element.
- CSS position property has four important values:

  - Static:
  - Absolute:
  - Relative: nudging elements or having an anchor
  - Fixed: fixed navigation or sidebars
  - Sticky: useful for navigation bars or headers

CSS Positioning does not get inherited as some other styles do: `.my-element {position: static | absolute | relative | fixed;}`

### `static` positioning

- Default positioning for elements
- Elements are built into the page from left to right, top to bottom

### `relative` positioning

- *Nudges* an element away from its resting position
- Element maintains the space it would have taken up if it was statically positioned

### CSS Float

#### Wrapping Text Around Images

- Elements can be floated, so they "stick" to the right/left while other inline elements flow around them
- `Float` was designed to allow inline elements to flow around other elements, such as images in a magazine.
- Do **NOT** use `float` for changing page layout
  - Modern solutions are much cleaner for page layout

### Useful Code

- `a:hover` is a CSS selector which allows you to change the color, background color, animation, etc for `<a>` tags when a mouse hovers over them.
- `transition` is a CSS rule which allows for basic animations to be applied when hovering over links
- `shape-outside:` is a CSS rule that allows for text to wrap around a floating element. Can be used for text to *curve* around a circle for example.
- `z-index` *(zed-index)*: controls how an image or element floats above or below other elements. Instead of an x-or-y axis it is using a z-axis which provides 3-dimensional effects to a webpage.

`Flexbox` for layout
`Positioning` for layering
`Float` for flow of content

***
***
***

# CONTENT BREAK

## BS Lecture: Typography and Fonts - `02/21/2023`

***

### Typography

- **Define**: The art and science of expressing hierarchy, brand presence, and personality.
- Choosing the right typography settings can make or break a design. **NO PAPYRUS OR COMIC CANS**
- There are several tools to help choose right fonts on a web page, however that is typically the domain of a graphic designer

### Typefaces

- Typeface is a collection of letters and symbols. Each character is unique, but will share a similar shape and form.
- Typeface is based mainly on the curvature of letters, numbers, etc.

### Font

- A font is a specific size, weight, or style of a typeface
- regular, **bold**, *italic*, ***bold italic***

### Serif Typefaces

- A serif is a small shape or projection which appears at the end of a stroke on a character. There are several different types.

### Sans-Serif Typefaces

- A font without serifs.
- There are several different types:
  - Grotesque, low contrast between thick and thin (work sans)
  - Humanist, medium contrast between thick and thin (Alegreya)
  - Geometric, low contrast between thick and thin, but with thicker verticals, and a softer rounded, mathematical feel (Comfortaa)

### Other Typefaces

**Monospaced**:

- All characters have the same width
- Great for code!
- Courier New, Roboto Mono, Consolas

**Handwriting**:

- Designed to look l

### Modifying Fonts

### Adjusting Font Size

**Using Absolute Units:**

- Use `px` units for each type element
- Allows direct control over element font sizes

**Using Relative Units:**

- Use % as a default size, declared within the root element (`html`) or omit altogether
- Then use `rem` units to relatively change the font size
- Allows for text elements to change dynamically & responsively
- Allows for the use of a modular scale system

### Adjusting `font-weight` and `font-style`

**font-weight**:

- the `font-weight` property sets the weight, or thickness of a font
- Accepts either a keyword value or predefined numeric value

**font-style**:

- The `font-style` property allows you to make text appear italicized
- Accepts one of three possible values: normal, italic, and oblique

### Adjusting Horizontal Space

- Use the CSS property: `letter-spacing`
- Can use negative or positive values to bring characters closer together or farther apart
- Tracking is the equivalent typography term, NOT kerning
- Don't adjust text at a paragraph level, use for headings or titles that are all caps.
- Niko used it on a paragraph for Lush which required FDA ingredients list on an order sheet. In order to make the paragraph fit he used `letter-spacing` and `line-height`

### Adjusting Vertical Space

- Use the CSS property: `line-height`
- Leading is the equivalent typography term
- Increasing line-height is a powerful way to increase legibility within verbose content & paragraphs
- Thick fonts, dark color fonts, long-form content can all benefit from increased line-heights

### `@font-face`

- An `at-rule` used to load a custom font-family into your site.
- The font can be loaded from a remote location, files in your project, or a locally installed font on the user's computer.
- Has two mandatory properties

  - `font-family`
  - `src`

### @font-face Demo

***
***
***

## BS Lecture: Animations - `02/25/2023`

### CSS Transitions

- Transitions are used to animate between different *states* of an element.
- Before it is hovered, an element is in an initial or "base" state.
- When hovering over an element (link or anchor tag), we can change the CSS properties so that they transition smoothly from one state to another

### Duration

- 
