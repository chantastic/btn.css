# btn.css

A scalable, styleable button.

## Installation

Scrit tag:

    <link rel="stylesheet" href="https://unpkg.com/btn.css@0.1.0" />

Node:

    npm install btn.css

## The code

This is `.btn` all the code.

    .btn {
      font-size: 1em;
      line-height: 2em;

      display: inline-block;

      padding: 0 1em;

      cursor: pointer;
      text-decoration: none;

      border-width: 1px;
      border-style: solid;
    }

## Usage

### Modifiers

Extend `.btn` with classes of your own.

Creating a new classes that define `color`, `background-color` and `border-color`.

    .my-fancy-outline-btn {
      color: purple;
      border-color: purple;
      background-color: transparent;
    }

### Adapters

Chances are you're buttons share a common theme.
Make an adapter for `.btn` in your app.

    /* my app's .btn */
    .btn {
      border-radius: 4px;
      box-shadow: 0 4px 3px -2px rgba(0,0,0,0.3);
    }
    .btn:hover { cursor: pointer }

### Scale

Scale `.btn` by changing `font-size`.

    .my-big-btn { font-size: 2em }

You can also scale one-off buttons right on element.

    <button class="btn" style="font-size: 20em">Super Button</button>

## More examples

[chantastic.org/btn.css](https://chantastic.org/btn.css/)

<3 [@chantastic](http://twitter.com/chantastic)