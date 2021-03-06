---
layout: page
title: "JavaScript is_int function"
comments: true
sharing: true
footer: true
alias:
- /functions/view/is_int:444
- /functions/view/is_int
- /functions/view/444
- /functions/is_int:444
- /functions/444
---
<!-- Generated by Rakefile:build -->
A JavaScript equivalent of PHP's is_int

{% codeblock var/is_int.js lang:js https://raw.github.com/kvz/phpjs/master/functions/var/is_int.js raw on github %}
function is_int (mixed_var) {
  // From: http://phpjs.org/functions
  // +   original by: Alex
  // +   improved by: Kevin van Zonneveld (http://kevin.vanzonneveld.net)
  // +    revised by: Matt Bradley
  // +   bugfixed by: Kevin van Zonneveld (http://kevin.vanzonneveld.net)
  // +   improved by: WebDevHobo (http://webdevhobo.blogspot.com/)
  // +   improved by: Rafał Kukawski (http://blog.kukawski.pl)
  // %        note 1: 1.0 is simplified to 1 before it can be accessed by the function, this makes
  // %        note 1: it different from the PHP implementation. We can't fix this unfortunately.
  // *     example 1: is_int(23)
  // *     returns 1: true
  // *     example 2: is_int('23')
  // *     returns 2: false
  // *     example 3: is_int(23.5)
  // *     returns 3: false
  // *     example 4: is_int(true)
  // *     returns 4: false

  return mixed_var === +mixed_var && isFinite(mixed_var) && !(mixed_var % 1);
}
{% endcodeblock %}

 - [Raw function on GitHub](https://github.com/kvz/phpjs/blob/master/functions/var/is_int.js)

Please note that php.js uses JavaScript objects as substitutes for PHP arrays, they are 
the closest match to this hashtable-like data structure. 

Please also note that php.js offers community built functions and goes by the 
[McDonald's Theory](https://medium.com/what-i-learned-building/9216e1c9da7d). We'll put online 
functions that are far from perfect, in the hopes to spark better contributions. 
Do you have one? Then please just: 

 - [Edit on GitHub](https://github.com/kvz/phpjs/edit/master/functions/var/is_int.js)

### Example 1
This code
{% codeblock lang:js example %}
is_int(23)
{% endcodeblock %}

Should return
{% codeblock lang:js returns %}
true
{% endcodeblock %}

### Example 2
This code
{% codeblock lang:js example %}
is_int('23')
{% endcodeblock %}

Should return
{% codeblock lang:js returns %}
false
{% endcodeblock %}

### Example 3
This code
{% codeblock lang:js example %}
is_int(23.5)
{% endcodeblock %}

Should return
{% codeblock lang:js returns %}
false
{% endcodeblock %}


### Other PHP functions in the var extension
{% render_partial _includes/custom/var.html %}
