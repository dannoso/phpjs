---
layout: page
title: "JavaScript strpos function"
comments: true
sharing: true
footer: true
alias:
- /functions/view/strpos:545
- /functions/view/strpos
- /functions/view/545
- /functions/strpos:545
- /functions/545
---
<!-- Generated by Rakefile:build -->
A JavaScript equivalent of PHP's strpos

{% codeblock strings/strpos.js lang:js https://raw.github.com/kvz/phpjs/master/functions/strings/strpos.js raw on github %}
function strpos (haystack, needle, offset) {
  // From: http://phpjs.org/functions
  // +   original by: Kevin van Zonneveld (http://kevin.vanzonneveld.net)
  // +   improved by: Onno Marsman
  // +   bugfixed by: Daniel Esteban
  // +   improved by: Brett Zamir (http://brett-zamir.me)
  // *     example 1: strpos('Kevin van Zonneveld', 'e', 5);
  // *     returns 1: 14
  var i = (haystack + '').indexOf(needle, (offset || 0));
  return i === -1 ? false : i;
}
{% endcodeblock %}

 - [Raw function on GitHub](https://github.com/kvz/phpjs/blob/master/functions/strings/strpos.js)

Please note that php.js uses JavaScript objects as substitutes for PHP arrays, they are 
the closest match to this hashtable-like data structure. 

Please also note that php.js offers community built functions and goes by the 
[McDonald's Theory](https://medium.com/what-i-learned-building/9216e1c9da7d). We'll put online 
functions that are far from perfect, in the hopes to spark better contributions. 
Do you have one? Then please just: 

 - [Edit on GitHub](https://github.com/kvz/phpjs/edit/master/functions/strings/strpos.js)

### Example 1
This code
{% codeblock lang:js example %}
strpos('Kevin van Zonneveld', 'e', 5);
{% endcodeblock %}

Should return
{% codeblock lang:js returns %}
14
{% endcodeblock %}


### Other PHP functions in the strings extension
{% render_partial _includes/custom/strings.html %}
