# annotator

This is an attempt at an accessible annotation scheme.

## Motovation

Visually annotating text is straightforward: draw each annotation in a style which stands out / is different from the surrounding text.  However, how does one do this in a way which supports screen readers? The only way I can think of is to surround the text to be annotated with some sort of marker. The issue of course is that if this marker also appears in the text to be annotated, the results will not be as the user expects.

Try the demo:
https://RichCaloggero.github.io/annotator/annotator.html


## Instructions

1. check the "enable annotator" button to enable editing
2. Put focus on the text via tab, find the start of text to be annotated and press the "*" (asterisk) key. A message will appear showing that you have successfully marked the start of the annotation.
3. Move to the end of the text to be annotated and again press "*".  Now you have an entry in the annotations list at the bottom of the page.  
	- Clicking an item in the list will select that text and focus the text area.  The screen reader will read the selected text when the element gains focus, the browser highlights the selection, and the caret is moved to the end of the selection.




You can change the text if you click the "enable text modification" checkbox.

You can add notes to whichever annotation is currently being displayed.

## Real world implementation

- we need to support user defined markers
- need to check to see if the marker exists in the text
- need to store the markers with the project and not let the user add them as part of the text
- need to be able to toggle their appearance within the text on demand
   + currently they are removed when an annotation is created and added to the list
   + clicking an annotation in the list jumps you to the correct spot in the text
   + toggling on inline annotations would insert them into the text so the user can hear annotations in context (not currently implemented)
