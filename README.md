<!-- @format -->

# Independent Challenge #1

## Responsive editorial article

For my first independent challenge, I created a responsive editorial article to strengthen my understanding of semantic HTML and typography.

The design uses typographic hierarchy, fluid font sizes, pseudo-elements, custom properties, and structural selectors.

You can find the Challenge [Here](../responsive-article/CHALLENGE.md).

---

## Project Goals

- Create a clear editorial hierarchy
- Maintain a comfortable reading width
- Use serif and sans-serif typefaces intentionally
- Create fluid typography
- Practice using semantic HTML
- Style article paragraphs according to their document structure
- Keep the page readable on narrow screens

---

## Built With

- Semantic HTML
- CSS custom properties
- `clamp()` for responsive typography
- Combinators and structural selectors
- Pseudo-classes
- Pseudo-elements
- CSS `float`

---

## Challenges and Solutions

### Targeting the Drop Cap

One of the main challenges I faced was positioning the drop cap and targeting it without adding unnecessary classes or HTML elements.

I solved this by learning how combinators, pseudo-classes, and pseudo-elements work together. The child combinator in `article > p` selects only paragraphs that are direct children of the article. This prevents paragraphs nested inside the header and footer from receiving the article-body styles.

I then used `:not()` and `:first-of-type` to distinguish the opening paragraph from the remaining paragraphs:

```css
article > p:not(:first-of-type) {
  text-indent: 1.5em;
}
```

Finally, I combined `:first-of-type` with the `::first-letter` pseudo-element to create the drop cap:

```css
article > p:first-of-type::first-letter {
  /* Drop-cap styles */
}
```

This allowed me to target the first letter of the opening paragraph without adding another class or wrapping element to the HTML.

### Positioning with float

This was also my first time using float independently. I applied `float: left` to the `::first-letter` pseudo-element so the enlarged letter would sit beside the first two opening lines instead of behaving like an ordinary inline letter..

The solution I created is shown below:

```css
article > p:first-of-type::first-letter {
  float: left;
  padding-top: 0.05em;
  padding-right: 0.15em;
  font-size: 3.2em;
  line-height: 0.8;
}
```

Getting the drop cap into the correct position required adjusting its font size, line height, and padding. This helped me understand how floated content affects the surrounding text.

### Responsive Sizing

Adjusting the typography for different screen sizes was another challenge. I initially relied too heavily on fixed `px` values. Through experimentation, I learned where relative units such as `rem`, `em`, viewport units, and percentages were more appropriate.

Using relative units let typography and spacing respond more naturally to changes in screen size and context. It also helped me understand that the best unit depends on what a value should be relative to, such as the root font size, the current element’s font size, or the viewport.

### Learning `clamp()`

I chose to use `clamp()` because I wanted to understand how fluid sizing works and how it supports responsive design.

Creating the values required experimentation, but I eventually arrived at a fluid headline size:

```css
--font-headline: clamp(1.8rem, 1.2rem + 2.5vw, 3.25rem);
```

The first value establishes the minimum size, the middle expression provides the fluid size, and the final value establishes the maximum size.

While experimenting, I discovered that `calc()` was unnecessary inside `clamp()` because `clamp()` already accepts a mathematical expression as an argument. I also found that lowering the minimum headline size to 1.8rem produced the narrow-screen result I wanted without requiring a separate media query.

Working through these problems took considerable research and experimentation, but it gave me a much clearer understanding of structural selectors, relative units, fluid typography, and responsive CSS.

---

## What I Learned

This challenge gave me practical experience with fluid typography, selector specificity, structural pseudo-classes, responsive sizing, floated elements, and CSS custom properties.

The biggest lesson was that HTML structure can simplify CSS. By using parent-child relationships and structural selectors, I was able to style the article without adding unnecessary classes.

I also learned that responsive design does not always require additional media queries. In this project, `clamp()` allowed the headline and other text to resize fluidly while remaining within the minimum and maximum sizes I selected.

Of everything I worked through, the broadest challenge was keeping my CSS organized as the stylesheet grew. Each solution introduced more variables, selectors, pseudo-classes, and declarations. Without a deliberate structure, the stylesheet could have quickly become difficult to read and maintain.

Grouping related custom properties, arranging styles in a logical order, and documenting helped keep the CSS from falling into chaos. I learned that organization is not something added after the code is finished — it is part of writing the code itself.

---

## Contributions

This is a personal learning project, but corrections and improvements are welcome through GitHub issues or pull requests.

Please keep contributions focused, explain what the change accomplishes, and avoid including unrelated modifications.

By submitting a contribution, you agree that your contribution may be distributed under the MIT License used by this project.

---

## License

This project — including its source code, documentation, and article text is available under the [MIT License](../responsive-article/LICENSE).
