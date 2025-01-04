# Uncommon HTML Bug: Setting innerHTML on Non-Existent Element

This repository demonstrates an uncommon bug in HTML where an attempt is made to modify the `innerHTML` of an element that does not yet exist in the Document Object Model (DOM).  The script executes without throwing an error, but the intended change does not occur, leading to unexpected behavior.

## Bug Description

The `bug.html` file contains a script that tries to set the `innerHTML` property of an element with the ID `myDiv2`. However, this element is not defined in the HTML structure.  Standard JavaScript error handling doesn't catch this; it silently fails.

## Solution

The `bugSolution.html` file presents a corrected version. It ensures the element exists before attempting to modify its `innerHTML` using either `document.createElement()` or checking if the element is already in the DOM before manipulating it.