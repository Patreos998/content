---
title: "ElementInternals: ariaLabel property"
short-title: ariaLabel
slug: Web/API/ElementInternals/ariaLabel
page-type: web-api-instance-property
browser-compat: api.ElementInternals.ariaLabel
---

{{APIRef("Web Components")}}

The **`ariaLabel`** property of the {{domxref("ElementInternals")}} interface reflects the value of the [`aria-label`](/en-US/docs/Web/Accessibility/ARIA/Reference/Attributes/aria-label) attribute, which defines a string value that labels the current Element.

> [!NOTE]
> Setting aria attributes on `ElementInternals` allows default semantics to be defined on a custom element. These may be overwritten by author-defined attributes, but ensure that default semantics are retained should the author delete those attributes, or fail to add them at all. For more information see the [Accessibility Object Model explainer](https://wicg.github.io/aom/explainer.html#default-semantics-for-custom-elements-via-the-elementinternals-object).

## Value

A string.

## Examples

In this example the value of `ariaLabel` is set to "close".

```js
class CustomControl extends HTMLElement {
  constructor() {
    super();
    this.internals_ = this.attachInternals();
    this.internals_.ariaLabel = "close";
  }
  // …
}
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
