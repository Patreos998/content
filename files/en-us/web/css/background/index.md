---
title: background
slug: Web/CSS/background
page-type: css-shorthand-property
browser-compat: css.properties.background
sidebar: cssref
---

The **`background`** [shorthand](/en-US/docs/Web/CSS/CSS_cascade/Shorthand_properties) [CSS](/en-US/docs/Web/CSS) property sets all background style properties at once, such as color, image, origin and size, or repeat method. Component properties not set in the `background` shorthand property value declaration are set to their default values.

{{InteractiveExample("CSS Demo: background")}}

```css interactive-example-choice
background: green;
```

```css interactive-example-choice
background: content-box radial-gradient(crimson, skyblue);
```

```css interactive-example-choice
background: no-repeat url("/shared-assets/images/examples/lizard.png");
```

```css interactive-example-choice
background: left 5% / 15% 60% repeat-x
  url("/shared-assets/images/examples/star.png");
```

```css interactive-example-choice
background:
  center / contain no-repeat
    url("/shared-assets/images/examples/firefox-logo.svg"),
  #eee 35% url("/shared-assets/images/examples/lizard.png");
```

```html interactive-example
<section id="default-example">
  <div id="example-element"></div>
</section>
```

```css interactive-example
#example-element {
  min-width: 100%;
  min-height: 100%;
  padding: 10%;
}
```

## Constituent properties

This property is a shorthand for the following CSS properties:

- {{cssxref("background-attachment")}}
- {{cssxref("background-clip")}}
- {{cssxref("background-color")}}
- {{cssxref("background-image")}}
- {{cssxref("background-origin")}}
- {{cssxref("background-position")}}
- {{cssxref("background-repeat")}}
- {{cssxref("background-size")}}

## Syntax

```css
/* Using a <background-color> */
background: green;

/* Using a <bg-image> and <repeat-style> */
background: url("test.jpg") repeat-y;

/* Using a <visual-box> and <'background-color'> */
background: border-box red;

/* A single image, centered and scaled */
background: no-repeat center/80% url("../img/image.png");

/* Global values */
background: inherit;
background: initial;
background: revert;
background: revert-layer;
background: unset;
```

The `background` property is specified as one or more background layers, separated by commas.

The syntax of each layer is as follows:

- Each layer may include zero or one occurrences of any of the following values:
  - `<attachment>`
  - `<bg-image>`
  - `<bg-position>`
  - `<bg-size>`
  - `<repeat-style>`

- The `<bg-size>` value may only be included immediately after `<bg-position>`, separated with the '/' character, like this: `center/80%`.
- The `<visual-box>` value may be included zero, one, or two times. If included once, it sets both {{cssxref("background-origin")}} and {{cssxref("background-clip")}}. If it is included twice, the first occurrence sets {{cssxref("background-origin")}}, and the second sets {{cssxref("background-clip")}}.
- The `<'background-color'>` value may only be included in the last layer specified.

### Values

- `<attachment>`
  - : See {{cssxref("background-attachment")}}. Default: `scroll`.
- `<visual-box>`
  - : See {{cssxref("background-clip")}} and {{cssxref("background-origin")}}. Default: `border-box` and `padding-box` respectively.
- `<'background-color'>`
  - : See {{cssxref("background-color")}}. Default: `transparent`.
- `<bg-image>`
  - : See {{Cssxref("background-image")}}. Default: `none`.
- `<bg-position>`
  - : See {{cssxref("background-position")}}. Default: 0% 0%.
- `<repeat-style>`
  - : See {{cssxref("background-repeat")}}. Default: `repeat`.
- `<bg-size>`
  - : See {{cssxref("background-size")}}. Default: `auto`.

The following three lines of CSS are equivalent:

```css
background: none;
background: transparent;
background: repeat scroll 0% 0% / auto padding-box border-box none transparent;
```

## Formal definition

{{cssinfo}}

## Formal syntax

{{csssyntax}}

## Accessibility

Browsers do not provide any special information on background images to assistive technology. This is important primarily for screen readers, as a screen reader will not announce its presence and therefore convey nothing to its users. If the image contains information critical to understanding the page's overall purpose, it is better to describe it semantically in the document.

- [MDN Understanding WCAG, Guideline 1.1 explanations](/en-US/docs/Web/Accessibility/Guides/Understanding_WCAG/Perceivable#guideline_1.1_—_providing_text_alternatives_for_non-text_content)
- [Understanding Success Criterion 1.1.1 | W3C Understanding WCAG 2.0](https://www.w3.org/TR/UNDERSTANDING-WCAG20/text-equiv-all.html)

## Examples

### Setting backgrounds with color keywords and images

#### HTML

```html
<p class="top-banner">
  Starry sky<br />
  Twinkle twinkle<br />
  Starry sky
</p>
<p class="warning">Here is a paragraph</p>
<p></p>
```

#### CSS

```css
.warning {
  background: pink;
}

.top-banner {
  background: url("star-solid.gif") #99f repeat-y fixed;
}
```

#### Result

{{EmbedLiveSample("Setting_backgrounds_with_color_keywords_and_images")}}

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{cssxref("box-decoration-break")}}
- [Using gradients](/en-US/docs/Web/CSS/CSS_images/Using_CSS_gradients)
- [Using multiple backgrounds](/en-US/docs/Web/CSS/CSS_backgrounds_and_borders/Using_multiple_backgrounds)
