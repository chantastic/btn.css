# btn.css

A singular, styleable button.

## Installation

Scrit tag:

    <link rel="stylesheet" href="https://unpkg.com/btn.css@0.1.0" />

Node:

    npm install btn.css

## The code

This is `.btn` all the code.

    .btn {
      display: inline-block;

      border-width: 1px;
      border-style: solid;

      padding: 0 1em;

      font-size: 1em;
      line-height: 2em;
      text-decoration: none;
    }

Extend it by creating a new classes that define `color`, `background-color` and `border-color`.

    .my-fancy-outline-btn {
      color: purple;
      border-color: purple;
      background-color: transparent;
    }

That's it.

You can also scale it by changing `font-size`.

    .my-big-btn { font-size: 2em }

[Examples](https://chantastic.org/btn.css/)

<3 [@chantastic](http://twitter.com/chantastic)