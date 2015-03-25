# Randomize Text
 [![License](http://img.shields.io/badge/License-MIT-blue.svg)](http://opensource.org/licenses/MIT)

### Takes a selector, randomizes the value for a random interval before revealing the original value.

***

### [→ CodePen Demo ←](http://codepen.io/anon/pen/MYLOre)
### [→ Demo File ←](https://github.com/gst4158/randomized_text/blob/master/demo.html)
***

Installation
------------
Simply place the index.html and script.js files into the same folder to see the randomization effect in motion.


Detailed Explaination
-----------
**This is designed to randomize only single letters and not full length words.**

How does it work? 

* Each iteration of the $('letters') selector is ran through the randomization script.

* Each element with a class of 'trueletter' has it's CSS set to display: none.

* All 'trueletter' elements are then cloned.

* The cloned element has the 'trueletter' class removed and the 'randomletter' class added.

* The cloned element's CSS is set to display: block.

* The cloned element is set as a variable so we can do stuff to it.

* A random interval variable is created with a max number of 200, and a minimum of 100.

* Counter variable is created so we can stop the randomization loop.

* Using a setInterval loop the 'randomletter' element has its text value randomly changed into letters, numbers, and symbols.

* Once the counter is greater or equal to the interval, the loop stops. The randomization is killed and hidden from view; and the 'trueletter' element has it's display set back to block.

