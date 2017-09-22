# Implementation
The intent of this base component is flexibility.

While that's the case, this is an opinionated look at implementation in an app.

## Action-derived button types
Composing classes should be named according to the action they perform.

This is the set I personally use in a crud app:

```css
/*
 * Spec:
 *   border: $color
 *   background: $color
 *   color: white
 */
.action-btn  { /* blue */ }
.create-btn  { /* green */ }
.destroy-btn { /* red */ }
```

To reduce the impact of color on a layout, `quiet` variants are used.
Where colors are particularly insulting (even in outline), use a gray `quiet` variant.

```css
/*
 * Spec:
 *   default:
 *     border: $color || $gray
 *     background: transparent
 *     color: $color || $gray
 *   hover:
 *     border: $color
 *     background: $color
 *     color: white
 */
.quiet-action-btn  { /* blue */ }
.quiet-create-btn  { /* green */ }
.quiet-destroy-btn { /* red */ }
```

## Generic button types
Not all buttons resut in a performed server action.
These are more "to taste" but this is how I see them.

### link-btn
A `.link-btn` is a layout convenince.

```css
/* Spec
 *   default:
 *     border: $color
 *     background: $color
 *     color: white
 *   hover:
 *     underline
 */
.link-btn { /* blue text */ }
```

### menu-btn
A `.menu-btn` is elements that toggle a menu.

```css
/* Spec
 *   dark-mono border
 *   gray background
 *   dark-mono text
 */
.link-btn { /* monochrome */ }
```

### subtle-action-btn
An `.subtle-action-btn` is used for generic actions.
It differs slightly from the gray-variant of the named action button.
It always starts gray and gains color.

```css
 * Spec:
 *   default:
 *     border: $gray
 *     background: transparent
 *     color: $gray
 *   hover:
 *     border: $blue
 *     background: transparent
 *     color: $blue
.action-btn { /* monochrome/blue */ }
```

## Sizing
The `.btn` base class is relative.
It always inherits size from the containing element.
That makes it mostly indifferent to global sizing techniques (`rem`, `px`, etc.)

The button should scale nicely (by default) simply by changing font-size:

```html
<button
  type="button"
  class="btn"
  style="font-size: 24px"
>
```

This gives you some reasonable flexibility when implementing on-off buttons that don't fit inside a system.

For highly repeated buttons, it can be useful to create some generic modifiers.

### Relative modifiers
These modifers simply nudge against the inherited font-size.

```css
.smaller-btn { font-size: smaller }
.larger-btn  { font-size: larger }
```

### Fixed
These modifiers are fixed to an application design system.
For the sake of example, I'll use `rem`-based font-scale.

```css
.xlarge-btn { font-size: 1.5rem }
.large-btn  { font-size: 1.25rem }
.medium-btn { font-size: 1rem }
.small-btn  { font-size: .875rem }
.xsmall-btn { font-size: .75rem }
```

## Extension
Flattness and composition is the goal.
For highly specific buttons, favor inline styles or utility classes

```html
<button
  type="button"
  class="create-btn btn"
  style="py-2 font-size-2"
>Create workflow card</button>
```

For highly specefic and reused styling, keep things flat.
Try to compose the smallest number of classes required.

```html
<button
  type="button"
  class="workflow-card-create-btn create-btn btn"
>Create workflow card</button>
```