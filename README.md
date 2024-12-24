# Uncommon HTML Bug: Accessing Element Before Parsing

This repository demonstrates an uncommon bug in HTML where an attempt is made to access and manipulate a DOM element before the browser has fully parsed and rendered it. This can lead to the element not being found or unexpected behavior.

## Bug Description

The bug occurs because the JavaScript code tries to access and modify the `myDiv` element before the browser has finished parsing the HTML.  This often happens when the script is placed before the element in the HTML.

## How to reproduce

1. Clone this repository.
2. Open `bug.html` in a web browser.
3. Observe that the `myDiv` element remains visible despite the JavaScript attempting to hide it. 

## Solution

The solution is to make sure the JavaScript code that interacts with the `myDiv` element is executed only *after* the element has been parsed.  The most common method is to place the script at the end of the body, or to use the `DOMContentLoaded` event.