# jquery.lastlineclass.js
A jQuery plugin for adding a class to the last line of a block of text. Kinda like what the ::first-line CSS pseudo-element does or what a ::last-line pseudo-element would do if it existed in CSS.

## How it works
Here is a simple setup:

```html
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.1.1/jquery.min.js"></script>
<script src="jquery.lastlineclass.js"></script>
<script>
  jQuery("p").lastlineclass({class:'myclass'});
</script>
```

This will add the `myclass` class to the last line of the paragraph

## Options
jquery.lastlineclass.js allows you to specify three optional values: `class`, `wordWrap` and `lastLineWrap`.

```javascript
jQuery("p").lastlineclass({ class: 'myclass', wordWrap: 'em', lastLineWrap: 'section' })
```

Default values are as follows. Change the wrapper elements if they are clashing with elements in your block of text:
```javascript
class : 'last-line-class'
wordWrap : 'span'
lastLineWrap : 'div'
```

## Notes

This script doesn't use line breaks to identify the last line, it wraps words (text occurring between spaces) in span elements (by default) and finds which are lowest on the page. This means that the last line is identified after the text has been rendered on screen. Unfortunately this means it doesn't hold up too well if you significantly modify the size or box model properties of the last line class compared with the rest of the text. My original use-case was to add an underline to the last line of a wordy heading and for the underline to appear only beneath the words, not beneath the full heading width (see demo link below).


## Demo

https://caitriona.github.io/jquery.lastlineclass.js/

