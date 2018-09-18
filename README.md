# CSS+JS LED Clock

This is a pretty straightfoward 24-hour clock built with CSS and vanilla JavaScript to replicate old-school LED clocks.

## CSS 7-segment displays

LED clock displays used a set of 7 horizontal and vertical bars to display a character, which are replicated here with a set of seven `segment` divs. These have an absolute position within a relatively-positioned `number` div. A set of six `number` divs make up the face of the clock, along with a pair of `colon` and a trio of `spacer` divs to group the hours, minutes, and seconds.

Inactive `segment`s are given a background colour of `#300`, and adding the `active` class to any `segment` "lights" it by changing the background colour to `#f00`, as well as giving it a `z-index` of 10 to bring it up from underneath any "unlit" segments. A slight `transition` delay to the background color is added for effect.

## Drawing digits with JavaScript

Every second, the time is updated and `drawNumber()` is called to refresh the clock display. To use the function, pass in the `number` div that you'd like updated, as well as the `digit` (0 through 9) to be displayed.

The bulk of the function is a `switch` statement that looks at the `digit` parameter, and then toggles the `active` class on the appropriate `segment` div to display it.

This `switch` statement can be easily extended to not only display digits but letters and symbols as well.

## Built on Glitch

**Glitch** is the friendly community where you'll build the app of your dreams. Glitch lets you instantly create, remix, edit, and host an app, bot or site, and you can invite collaborators or helpers to simultaneously edit code with you.

Find out more [about Glitch](https://glitch.com/about).

## To Do

- Right now this is fixed at 1000px wide by 250px high. It'd be nice to make this responsive to screen size.
- A 12/24-hour toggle would be nice.
- A [16-segment display](https://en.wikipedia.org/wiki/Sixteen-segment_display) would allow for the display of more characters and symbols.