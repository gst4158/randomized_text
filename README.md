# Randomize Text
 [![License](http://img.shields.io/badge/License-MIT-blue.svg)](http://opensource.org/licenses/MIT)

### Takes a selector, randomizes the value for a random interval, hides the random value, and reveals the true value afterwards.

***

### [→ Demo ←](http://google.com)

***

Installation
------------
Simple copy/paste the index.html and script.js files into the same folder to see the randomization effect in motion.


Detailed Explaination
-----------

How does it work? 

* Wrap letters in any container you want with the 'letters' class.

* This will hook into jQuery and clone that element.

* jQuery takes the cloned element and starts randomizing it by a random interval (min of 100 and max of 200 in this demo). 

* Once the counter reaches higher than the interval, the randonized letter is hidden, and our true letter is revealed.

