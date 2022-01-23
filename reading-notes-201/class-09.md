# Notes - Day 9

_Ch.7 "Forms"_

Form controls: Adding text, text input, password input. Making choices: buttons, checkboxes, drop-down boxes. Submitting buttons. File uploads

Forms allow users to submit information.

`<form>`= carries action attribute & usually has method or id.

`<action>`= is url tag to another page.

`<input>`

`<text-type>`= name, length= used to put a max on characters. 

`<type-password>`= name, max-length

`<text-area>`= used to create the box text will be entered into.

`<type-radio>`= name, value, checked.

`<type-checkbox>`= name, value, checkbox.

`<Drop-down box>`= known as `<select>`

`<Multiple>`= allows to select multiple. size= used to show how many options on screen.

`<option>`= value

If long list use drop-down list. If user needs to see all options at once use radio.

`<type-file>`, `<type-submit>`

`<type-image>`= use for image of `<button>`

`<type-hidden>`= not seen in browser window, unless you view source.

`<label>`= used for screen readers. Best places for labels are above or to the left: `<text-input>`, `<text-area>` `<select-boxes>` `<file-uploads>`

To the right; individual checkboxes & radio

`<field-set>`= group together related items. `<legend>`= after field & contains option or purpose

`<form-validation>`= used to make sure form filled out correctly

`<type-date>`=creates date input

`<type-email>`= verifies correct email address format.

`<type-url>`= format of url

`<type-search>`= search box

`<placeholder>`= text in search box until the user enters input.

_Ch.14 "Lists, Tables & Forms"_

`<list-style-type>`= used to apply to lists

`<list-style-image>`=used on ul & li elements

`<list-style-position>`= outside or inside

`<empty-cells>`= show, hide, or inherit

`<border-spacing>`=adds some space between cells `<border-collapse>`= will collapse to 1 line `<separate>`= borders don't touch.

_Ch.15 "Events"_

Different event types (Ref. on pg 246-247, Jon Duckett, JavaScript & JQuery.)

Events are "fired" or "raised" when clicked on, and trigger scripts or functions.

Event Handling How events are triggered: 1) Select element 2) indicate which event, called binding 3) state code to run

3 event handlers= HTML handlers, Traditional DOM event handlers, which could only trigger 1 function per event handler & DOM level 2 event Listeners, which can do multiple

When using event handlers, event is preceded by the word "on" in HTML

Can't use or pass arguments in event listeners. To bypass, make a function, then wrap it in another function.

For older version of IE,. use if...else statements. If eventListener() is there, else attachEvent().

Event bubbling starts at most specific node & goes out.

Event capturing starts at least specific node & goes in.

Event delegation= Event listeners use lots of memory. Try to put it on the parent element and repeat for children as opposed to 1 on each child.

Benefits of event delegation is it works with new elements, solves limitations with .this keyword & simplifies code.

Different DOM types can be ref - (Ref. on pg 271-287, Jon Duckett, JavaScript & JQuery.)

User interface events, load, focus & blur, mouse, click, keyboard, form, mutations & observers, HTML5.

**<a href = "https://github.com/scottie-l/reading-notes/blob/main/reading-notes-201/README.md">Back</a>**
