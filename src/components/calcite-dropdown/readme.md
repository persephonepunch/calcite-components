# calcite-dropdown

Calcite-dropdown can be used to provide an absolutely positioned set of selectable items. You can combine multiple groups of items and selection modes, and optionally pass a title for each group. All `<calcite-dropdown-item>` must have a parent `<calcite-dropdown-group>`, even if `group-title` attribute is not set.

A basic implementation looks like this:

```html
<calcite-dropdown>
  <calcite-button slot="dropdown-trigger">Open Dropdown</calcite-button>
  <calcite-dropdown-group>
    <calcite-dropdown-item>Relevance</calcite-dropdown-item>
    <calcite-dropdown-item active>Date modified</calcite-dropdown-item>
    <calcite-dropdown-item>Title</calcite-dropdown-item>
  </calcite-dropdown-group>
</calcite-dropdown>
```

You can combine groups in a single dropdown, with varying selection modes:

```html
<calcite-dropdown>
  <calcite-button slot="dropdown-trigger">Open Dropdown</calcite-button>
  <calcite-dropdown-group group-title="Select one">
    <calcite-dropdown-item>Apple</calcite-dropdown-item>
    <calcite-dropdown-item active>Orange</calcite-dropdown-item>
    <calcite-dropdown-item>Grape</calcite-dropdown-item>
  </calcite-dropdown-group>
  <calcite-dropdown-group group-title="Select multi" selection-mode="multi">
    <calcite-dropdown-item>Asparagus</calcite-dropdown-item>
    <calcite-dropdown-item active>Potato</calcite-dropdown-item>
    <calcite-dropdown-item>Yam</calcite-dropdown-item>
  </calcite-dropdown-group>
  <calcite-dropdown-group
    group-title="Select none (useful for actions)"
    selection-mode="none"
  >
    <calcite-dropdown-item>Plant beans</calcite-dropdown-item>
    <calcite-dropdown-item active>Add peas</calcite-dropdown-item>
  </calcite-dropdown-group>
</calcite-dropdown>
```

<!-- Auto Generated Below -->

## Properties

| Property        | Attribute   | Description                                                                             | Type                               | Default     |
| --------------- | ----------- | --------------------------------------------------------------------------------------- | ---------------------------------- | ----------- |
| `active`        | `active`    |                                                                                         | `boolean`                          | `false`     |
| `alignment`     | `alignment` | specify the alignment of dropdown, defaults to start                                    | `"center" \| "end" \| "start"`     | `"start"`   |
| `maxItems`      | `max-items` | specify the max items to display before showing the scroller, must be greater than 0 \* | `number`                           | `0`         |
| `scale`         | `scale`     | specify the scale of dropdown, defaults to m                                            | `"l" \| "m" \| "s"`                | `"m"`       |
| `selectedItems` | --          | **read-only** The currently selected items                                              | `HTMLCalciteDropdownItemElement[]` | `[]`        |
| `theme`         | `theme`     | specify the theme of the dropdown, defaults to light                                    | `"dark" \| "light"`                | `undefined` |
| `type`          | `type`      | specify whether the dropdown is opened by hover or click of the trigger element         | `"click" \| "hover"`               | `"click"`   |
| `width`         | `width`     | specify the width of dropdown, defaults to m                                            | `"l" \| "m" \| "s"`                | `"m"`       |

## Events

| Event                   | Description                                     | Type                |
| ----------------------- | ----------------------------------------------- | ------------------- |
| `calciteDropdownSelect` | fires when a dropdown item has been selected \* | `CustomEvent<void>` |

## Dependencies

### Used by

- [calcite-split-button](../calcite-split-button)

### Graph

```mermaid
graph TD;
  calcite-split-button --> calcite-dropdown
  style calcite-dropdown fill:#f9f,stroke:#333,stroke-width:4px
```

---

_Built with [StencilJS](https://stenciljs.com/)_
