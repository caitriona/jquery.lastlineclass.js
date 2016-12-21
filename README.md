# jquery.lastlineclass.js
A jQuery plugin for adding a specified class to the last line of a block of text

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

## options
jquery.lastlineclass.js allows you to specify three optional values: `class`, `wordWrap` and `lastLineWrap`.

```javascript
jQuery("p").lastlineclass({ class: 'myclass', wordWrap: 'em', lastLineWrap: 'section' })
```

Default values are as follows. Change the wrapper elements only if they are clashing with elements in your block of text:
class : 'last-line-class'
wordWrap : 'span'
lastLineWrap : 'div'

## Notes

The script does not use line breaks to identify the last line, the contents of the last line is identified after the text has been rendered on the page. One issue with this is that it doesn't hold up too well to if you significantly modify the box model or size properties of the last line class compared with the rest of the text.



