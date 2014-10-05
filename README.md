jquery-style
============

jquery plugin for altering stylesheets

How to use:

1. Add rule to stylesheet:

addRule(name, style, index)
name - rule selector
style - rule styles as a string or style name and value pair object
index - (optional)position of the inserted rule within the stylesheet

Examples:
  $('#my-stylesheet').styleSheet().addRule('p', 'color: red; font-weight: bold')
  
Or

  $('#my-stylesheet').styleSheet().addRule('p', {'color': 'red', 'font-weight': 'bold'})
  
Or

  $('#my-stylesheet').addCssRule('p', {'color': 'red', 'font-weight': 'bold'})

2. Remove rule from stylesheet:

remove(index)
index - (optional)index of the rule within the parent stylesheet

Example:

  $('#my-stylesheet').styleSheet().rule('p').remove();
  
Or

  $('#my-stylesheet').styleSheet().rule('p').remove(0);
  
Or

  $('#my-stylesheet').styleSheet().rule('p', 0).remove();

Or  

  $('#my-stylesheet').removeCssRule('p');

Or

  $('#my-stylesheet').removeCssRule('p', 0);

3. Alter rule

css(name) - returns value of specified style from the first rule in the list
name - style name in css format (for example "background-color")

Example:

  $('#my-style').styleSheet().rule('p').css('color')

css(name, value) - set specified style to provided value for all rules within the list
name - style name in css format
value - new value for specified style
index - (optional)ruile index within the parent stylesheet

Example:

  $('#my-style').styleSheet().rule('p').css('color', 'red')

OR

	Example: $('#my-style').styleSheet().rule('p').css('color', 'red', 0)

css(data) - set multiple styles for all rules in the list using an object (for example {'color' : 'red', 'font-weight' : 'bold'})
data - object containing style name and value pairs
index - (optional)rule index within the parent stylesheet

Example:

  $('#my-style').styleSheet().rule('p').css({'color' : 'red', 'font-weight' : 'bold'})

Or

	Example: $('#my-style').styleSheet().rule('p').css({'color' : 'red', 'font-weight' : 'bold'}, 0)
	
4. Select rule

TO BE CONTINUED...

This plugin is available under the WTFPL (http://pl.wikipedia.org/wiki/WTFPL) license.
