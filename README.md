jquery-style
============

jquery plugin for altering stylesheets

Basically it's somethin similar to https://github.com/f0r4y312/jquery-stylesheet

<h2>How to use:</h2>

<h4>1. Add rule to stylesheet:</h4>

<b>addRule(name, style, index)</b><br/>
<ul>
<li>name - rule selector</li>
<li>style - rule styles as a string or style name and value pair object</li>
<li>index - <i>(optional)</i>position of the inserted rule within the stylesheet</li>
</ul>

<b>Examples:</b>

	$('#my-stylesheet').styleSheet().addRule('p', 'color: red; font-weight: bold')
  
Or

	$('#my-stylesheet').styleSheet().addRule('p', {'color': 'red', 'font-weight': 'bold'})
  
Or

	$('#my-stylesheet').addCssRule('p', {'color': 'red', 'font-weight': 'bold'})

<h4>2. Remove rule from stylesheet:</h4>

<b>remove(index)</b><br/>
<ul>
<li>index - <i>(optional)</i>index of the rule within the parent stylesheet</li>
</ul>

<b>Example:</b>

	$('#my-stylesheet').styleSheet().rule('p').remove();
  
Or

	$('#my-stylesheet').styleSheet().rule('p').remove(0);
  
Or

	$('#my-stylesheet').styleSheet().rule('p', 0).remove();

Or  

	$('#my-stylesheet').removeCssRule('p');

Or

	$('#my-stylesheet').removeCssRule('p', 0);

<h4>3. Alter rule</h4>

<b>css(name)</b> - returns value of specified style from the first rule in the list<br/>
<ul>
<li>name - style name in css format (for example "background-color")</li>
</ul>

<b>Example:</b>

	$('#my-style').styleSheet().rule('p').css('color')

<b>css(name, value)</b> - set specified style to provided value for all rules within the list<br/>
<ul>
<li>name - style name in css format</li>
<li>value - new value for specified style</li>
<li>index - <i>(optional)</i>ruile index within the parent stylesheet</li>
</ul>

<b>Example:</b>

	$('#my-style').styleSheet().rule('p').css('color', 'red')
	
OR

	$('#my-style').cssRule('p').css('color', 'red')

OR

	$('#my-style').styleSheet().rule('p').css('color', 'red', 0)

OR

	$('#my-style').cssRule('p').css('color', 'red', 0)

<b>css(data)</b> - set multiple styles for all rules in the list using an object</br>
<ul>
<li>data - object containing style name and value pairs</li>
<li>index - <i>(optional)</i>rule index within the parent stylesheet</li>
</ul>

<b>Example:</b>

	$('#my-style').styleSheet().rule('p').css({'color' : 'red', 'font-weight' : 'bold'})
	
OR
	
	$('#my-style').cssRule('p').css({'color' : 'red', 'font-weight' : 'bold'})
	
OR

	$('#my-style').styleSheet().rule('p').css({'color' : 'red', 'font-weight' : 'bold'}, 0)

OR
	
	$('#my-style').cssRule('p').css({'color' : 'red', 'font-weight' : 'bold'}, 0)
	
<h4>4. Select rule</h4>

<b>rule(name, index)</b>
<ul>
<li>name - selector to match</li>
<li>index - index - <i>(optional)</i>rule index within the parent stylesheet</li>
</ul>

<b>Example:</b>

	$('#my-stylesheet').styleSheet().rule('p')
	
OR

	$('#my-stylesheet').cssRule('p')

OR

	$('#my-stylesheet').styleSheet().rule('p', 0)

OR

	$('#my-stylesheet').cssRule('p', 0)
	
<h4>For more information about the plugin check the nonminified js file, I've left some additional comments there.</h4>
	
<h2>LICENSE</h2>

This plugin is available under the WTFPL (http://pl.wikipedia.org/wiki/WTFPL) license.
