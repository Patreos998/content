---
title: "ElementInternals: ariaValueText property"
short-title: ariaValueText
slug: Web/API/ElementInternals/ariaValueText
page-type: web-api-instance-property
browser-compat: api.ElementInternals.ariaValueText
---

{{APIRef("Web Components")}}

The **`ariaValueText`** property of the {{domxref("ElementInternals")}} interface reflects the value of the [`aria-valuetext`](/en-US/docs/Web/Accessibility/ARIA/Reference/Attributes/aria-valuetext) attribute, which defines the human-readable text alternative of aria-valuenow for a range widget.

> [!NOTE]
> Setting aria attributes on `ElementInternals` allows default semantics to be defined on a custom element. These may be overwritten by author-defined attributes, but ensure that default semantics are retained should the author delete those attributes, or fail to add them at all. For more information see the [Accessibility Object Model explainer](https://wicg.github.io/aom/explainer.html#default-semantics-for-custom-elements-via-the-elementinternals-object).

## Value

A string.

## Examples

In this example the value of `ariaValueText` is set to "Sunday".

```js
class CustomControl extends HTMLElement {
  constructor() {
    super();
    this.internals_ = this.attachInternals();
    this.internals_.ariaValueText = "Sunday";
  }
  // …
}
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
