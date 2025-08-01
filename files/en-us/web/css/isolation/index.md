---
title: isolation
slug: Web/CSS/isolation
page-type: css-property
browser-compat: css.properties.isolation
sidebar: cssref
---

The **`isolation`** [CSS](/en-US/docs/Web/CSS) property determines whether an element must create a new {{glossary("stacking context")}}.

{{InteractiveExample("CSS Demo: isolation")}}

```css interactive-example-choice
isolation: auto;
```

```css interactive-example-choice
isolation: isolate;
```

```html interactive-example
<section class="default-example" id="default-example">
  <div class="background-container">
    <div id="example-element">
      <img src="/shared-assets/images/examples/firefox-logo.svg" />
      <p><code>mix-blend-mode: multiply;</code></p>
    </div>
  </div>
</section>
```

```css interactive-example
.background-container {
  background-color: #f4f460;
  width: 250px;
}

#example-element {
  border: 1px solid black;
  margin: 2em;
}

#example-element * {
  mix-blend-mode: multiply;
  color: #8245a3;
}
```

This property is especially helpful when used in conjunction with {{cssxref("mix-blend-mode")}} and {{cssxref("z-index")}}.

## Syntax

```css
/* Keyword values */
isolation: auto;
isolation: isolate;

/* Global values */
isolation: inherit;
isolation: initial;
isolation: revert;
isolation: revert-layer;
isolation: unset;
```

The `isolation` property is specified as one of the keyword values listed below.

### Values

- `auto`
  - : A new stacking context is created only if one of the properties applied to the element requires it.
- `isolate`
  - : A new stacking context must be created.

## Formal definition

{{cssinfo}}

## Formal syntax

{{csssyntax}}

## Examples

### Forcing a new stacking context for an element

#### HTML

```html
<div class="big-square">
  <div class="isolation-auto">
    <div class="small-square">auto</div>
  </div>
  <div class="isolation-isolate">
    <div class="small-square">isolate</div>
  </div>
</div>
```

#### CSS

```css
.isolation-auto {
  isolation: auto;
}

.isolation-isolate {
  isolation: isolate;
}

.big-square {
  background-color: rgb(0 255 0);
  width: 200px;
  height: 210px;
}

.small-square {
  background-color: rgb(0 255 0);
  width: 100px;
  height: 100px;
  border: 1px solid black;
  padding: 2px;
  mix-blend-mode: difference;
}
```

#### Result

{{ EmbedLiveSample('Forcing_a_new_stacking_context_for_an_element', 230, 230) }}

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{cssxref("&lt;blend-mode&gt;")}}
- {{cssxref("mix-blend-mode")}}, {{cssxref("background-blend-mode")}}
