# Randomize Text
 [![License](http://img.shields.io/badge/License-MIT-blue.svg)](http://opensource.org/licenses/MIT)

### Takes a selector, randomizes the value for a random interval, hides the random value, and reveals the true value afterwards.

***

### [→ CodePen Demo ←](http://codepen.io/anon/pen/MYLOre)
### [→ Demo File ←](https://github.com/gst4158/randomized_text/blob/master/demo.html)
***

Installation
------------
Simple copy/paste the index.html and script.js files into the same folder to see the randomization effect in motion.


Detailed Explaination
-----------
**This will only work on single letters. Any words will be hidden from view while randomization animation is going on.**

How does it work? 

* Hooking int othe 'letters' selector we use jQuery to go through each iteration and randomize the letter.

* Our element is then cloned, removes the 'trueletter' class, adds the 'randomletter' class, and sets the clonned element to display: block. We set this cloned element as a variable so we can do stuff to it.

* Needing a time limit to randomize the text, a random interval is created with a max number of 200, and a minimum of 100.

* Using a setInterval loop the 'randomletter' element has its text value randomly changed into letters, numbers, and symbols.

* Once the counter is greater or equal to the interval, the loop stops. The randomization is killed and hidden from view; and the 'trueletter' element has it's display set back to block.

