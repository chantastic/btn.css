# btn.css

A general purpose, extensible button class with themes.

## Usage

This is a minimum viable button in its entirety.

    .btn,
    .btn:link,
    .btn:visited {
      display: inline-block;

      border-width: 1px;
      border-style: solid;

      padding: 0 1em;

      font-size: 1em;
      line-height: 2em;
      text-decoration: none;
    }

It has very few opinions about anything.

You extend it by creating a new classes that define `color`, `background-color` and `border-color`.

    .my-fancy-outline-btn {
      color: purple;
      border-color: purple;
      background-color: transparent;
    }

That's pretty much it.

## Contextual style

I [utility classes for everything](https://github.com/chantastic/minions.css).
So, there are no general-purpose modifiers for the `.btn` base class.

### Scaling

If you want to scale the button, apply a different `font-size`.

## Included classes

There are a few classes bundled in by default.

* `.default-btn`
* `.action-btn`
* `.quiet-action-btn`
* `.create-btn`
* `.quiet-create-btn`
* `.destroy-btn`
* `.quiet-destroy-btn`

[Examples](https://chantastic.org/btn.css/)

<3 [@chantastic](http://twitter.com/chantastic)