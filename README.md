# Uncommon HTML Bug: JavaScript DOM Manipulation Timing Issue

This repository demonstrates a subtle bug that can occur in HTML when JavaScript code attempts to interact with a DOM element before the element has been fully parsed and added to the DOM tree.

## Bug Description
The bug arises from incorrect ordering of the script tag and the element it's trying to access. The script executes *before* the element with the ID "myDiv" is fully parsed, resulting in an error or unexpected behavior.

## Bug Reproduction
1. Clone the repository.
2. Open the `bug.html` file in a web browser.
3. Observe that the text within the div element is not visible.

## Solution
The solution involves ensuring that the JavaScript code that manipulates the element is executed only after the element has been completely loaded and added to the DOM.  This is achieved by placing the script at the end of the body, or by using the DOMContentLoaded event listener.  The correct code and example can be found in `bugSolution.html`.

## Contributing
Feel free to contribute if you have suggestions or enhancements!