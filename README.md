# Splendid

Splendid is a simple jQuery textbox editor. It isn't a WYSIWYG so if that's what you're after then leave now. Splendid allows you to replace text with things like BBCode, Markdown, Textile or whatever you fancy. Simply create some custom mappings and you're away.

## Maps

Splendid uses maps to associate different items with specific actions. Let's take a look at an example map.

~~~~
bold: {
	placeholder: 'Bold',
	before: '**',
	after: '**',
	class: 'bold'
}
~~~~

The name for this property is 'bold', and we assign an object to this property. The object can have a number of different properties, the most basic is shown.

##### placeholder
Placeholder text is inserted when no text is selected. After the placeholder is inserted it is then selected so users can begin editing the text as quickly as possible.

##### before
This is the text to be placed before the selected text, or before the cursor if no text is selected.

##### after
This is the text to be placed after the selected text, or after the cursor if no text is selected.

##### replace
This is the text that will replace the selected text, or just insert at the cursors current position.

##### class
Each item can be assigned a unique class to assist with styling.

### Custom Prompts
It's often nice to request input from the user, say for example when inserting a hyperlink. Splendid allows simple prompts to be displayed to users asking for input. The syntax is as follows.

~~~~
[@Title:default]
~~~~

Example:

~~~~
[@URL:http://]
~~~~

## Examples

Inserting a markdown styled hyperlink at the current cursor position.

~~~~
link: {
	placeholder: 'Link',
	before: '[',
	after: ']([@URL:http://] "[@Title]")',
	class: 'link'
}
~~~~

Inserting a BBCode styled hyperlink at the current cursor position.

~~~~
link: {
	placeholder: 'Link',
	before: '[url=[@URL:http://]]',
	after: '[/url]',
	class: 'link'
}
~~~~