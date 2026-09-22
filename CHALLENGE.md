# Responsive Editorial Article Challenge

## Challenge Overview

Create a responsive editorial article using semantic HTML and CSS. The main focus of the challenge is typography: establish a clear reading hierarchy, create a comfortable measure for long-form text, and make the type scale respond naturally across screen sizes.

The completed page should feel like a carefully designed newspaper or literary-journal article rather than a generic webpage.

---

### Skills to Practice

- Semantic HTML

- Typographic hierarchy

- Serif and sans-serif font pairing

- Readable line length and line height

- Relative CSS units

- Fluid typography

- CSS custom properties

- Combinators and structural selectors

- Pseudo-classes and pseudo-elements

- Responsive design

---

### Project Requirements

#### HTML Structure

##### Document structure

1. Include a valid HTML document with the appropriate language declaration.
2. Include one `main` element.
3. Place the complete feature inside an `article`.
4. Use exactly one `h1`.
5. Use semantic elements wherever an appropriate one exists.
6. Use a `blockquote` for the pull quote.
7. Use a `footer` for the closing note.
8. Do not use an element solely to make text bold or italic.
9. Do not use inline CSS.
10. A `div` may be used only when no more meaningful semantic element applies.

##### Base typography

11. Set the root font size to `18px`.
12. Give the document a serif default font.
13. Set the default text color to Ink.
14. Use at least three different font sizes.
15. Use at least three different font weights.
16. Use at least two different line heights.
17. Use both `rem` and `em` units appropriately.
18. Keep the article’s readable line length between approximately 55 and 75 characters.

##### Publication name

19. Display the publication name in uppercase using CSS.
20. Use the sans-serif font stack.
21. Add visible letter spacing.
22. Make it prominent without allowing it to compete with the headline.

##### Issue information

23. Use the sans-serif font stack.
24. Display it in Muted ink.
25. Make it smaller than the main article text.
26. Add letter spacing to distinguish it from ordinary paragraphs.

##### Headline

27. Make the headline the largest text on the page.
28. Use the serif font stack.
29. Use a tighter line height than the article paragraphs.
30. Do not use `text-transform: uppercase` on the headline.
31. Ensure that a two-line headline would have comfortable spacing.

##### Introductory summary

32. Make the summary larger than the article paragraphs but smaller than the headline.
33. Give it a distinct style using weight, style, color, or a combination of those properties.
34. Use a comfortable line height.

##### Author and date information

35. Make the author’s name visibly stronger than the surrounding metadata.
36. Use the sans-serif font stack for both pieces of information.
37. Display the date and reading time in Muted ink.
38. Do not use an additional heading element for this information.

##### Article paragraphs

39. Use a line height of at least 1.6.
40. Separate paragraphs through indentation, vertical spacing, or a deliberate combination of both.
41. Do not indent the first article paragraph.
42. Indent the remaining ordinary article paragraphs using an `em` value.
43. Use a pseudo-class or sibling selector to control which paragraphs are indented.
44. Do not add a separate class to every paragraph.

##### First letter

45. Style the first letter of the first article paragraph with `::first-letter`.
46. Make it noticeably larger and bolder than the surrounding text.
47. Apply the Copper color to it.
48. Ensure that the first line remains readable.

##### Pull quote

49. Make the pull quote visually distinct from the article paragraphs.
50. Use the Copper color as an accent.
51. Increase its font size.
52. Use a tighter line height than the article paragraphs.
53. Remove the browser’s default blockquote margin and replace it intentionally.
54. Add quotation marks through CSS pseudo-elements rather than typing them into the provided content.

##### Closing note

55. Separate the closing note from the article with a visible rule.
56. Make it smaller than the main article text.
57. Use the sans-serif font stack.
58. Display it in Muted ink.

#### Restrictions

- No Flex-box
- No Grid
- No positioning
- No JavaScript
- No external fonts
- No CSS framework
- No inline CSS
- No `<br>` elements for visual spacing
- No empty elements used as decoration
- No changes to the supplied wording
- No media query required

Normal document flow, margins, padding, borders, widths, and `max-width` are allowed.

#### Visual success checks

- Your solution is successful when:
- The headline is the obvious first reading point.
- The publication name is recognizable but secondary.
- The summary is visually separate from the article body.
- The metadata is readable without drawing unnecessary attention.
- Paragraphs can be read comfortably without losing one’s place.
- The pull quote interrupts the article without overpowering it.
- Serif and sans-serif typefaces have clearly defined roles.
- Spacing feels consistent rather than randomly assigned.
- The page has no horizontal scrollbar at narrow widths.
- The design remains readable when the browser is zoomed to 200%.

##### Optional stretch goals

After completing the core requirements:

- Use `clamp()` to make the headline scale with the viewport.
- Style selected text with `::selection`.
- Add a decorative divider using `::before` or `::after`.
- Use `font-variant-caps` on the publication name or metadata.
- Add a single media query that reduces the headline size on very narrow screens.

### Supplied Design Assets

#### Color Palette

| Purpose                    | Color     |
| -------------------------- | --------- |
| Paper                      | `#f4efe5` |
| Ink                        | `#24211d` |
| Muted ink                  | `#6d665d` |
| Copper accent              | `#9a4f2e` |
| Rule and subtle background | `#c8bca9` |

### Decorative character

You may use this character as a divider: `◆`

You may place it in the HTML or generate it with a pseudo-element.

### Font Stacks

- Editorial serif: `Georgia, "Times New Roman", serif`
- Supporting sans serif: `Arial, Helvetica, sans-serif`

No image assets are required.

## Supplied Content

### Publication

The Craft Ledger

Volume 01 · Issue 04 · Peoria, Arizona

### Section

#### Kicker/Eyebrow

Back of House

#### Headline

The Kitchen Before Service

#### Deck Head

Before the first plate reaches the dining room, the kitchen has already told you what kind of night it will be.

#### Byline

Written by: John Doe

September 20, 2026 · 6 minute read

#### Article

A professional kitchen does not begin with fire. It begins with quiet preparation: knives being sharpened, towels being folded, sauces being checked, and cooks arranging their stations in ways that make sense to their hands. These small acts rarely appear in photographs, yet they determine nearly everything that follows.

Mise en place is often translated as “everything in its place,” but the phrase describes more than organization. It is a way of thinking ahead. Each ingredient is prepared before it is needed, each tool is kept within reach, and each movement is considered before the pressure of service begins.

#### Pull Quote

Preparation creates enough order for the cook to respond intelligently when that order is disturbed.

#### Article Continued

Preparation does not remove uncertainty. A dining room can fill without warning, a sauce can break, or a delivery can arrive incomplete. Good preparation creates enough order for the cook to respond intelligently when that order is disturbed.

Experience becomes visible in these moments. The experienced cook does not necessarily move faster than everyone else. Instead, unnecessary movement disappears. The cook reaches for the correct pan, notices a problem before it becomes a failure, and understands which details require immediate attention.

Long before the first ticket arrives, the standard has already been established. It lives in the clean cutting board, the labeled container, the tasted sauce, and the station prepared for a rush that may or may not come. Service merely reveals the quality of the work that was done while the kitchen was still quiet.

#### Field Note

From the Field Notes series: observations on craft, discipline, and the knowledge earned through repetition.

### Reflection

1. After completing the challenge, document:
2. Which part of the typography was hardest to control?
3. Which selectors helped you style the document without adding extra markup?
4. Where did relative units work better than fixed units?
5. How did you determine the minimum, preferred, and maximum values for fluid type?
6. What would you organize or document differently in your next project?
