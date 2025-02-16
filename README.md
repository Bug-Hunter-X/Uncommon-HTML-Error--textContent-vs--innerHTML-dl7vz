# Uncommon HTML Error: textContent vs. innerHTML

This repository demonstrates a subtle but important difference between using `textContent` and `innerHTML` when manipulating the content of HTML elements.  Incorrect usage of `textContent` can lead to unexpected behavior and security vulnerabilities, especially when dealing with user-supplied data.

## The Bug

The `bug.html` file shows an example where `textContent` is used to update the content of a div element. While seemingly innocuous, this approach can fail to properly render HTML content within the div.

## The Solution

The `bugSolution.html` file demonstrates the correct approach using `innerHTML` to handle HTML content safely. This ensures that any HTML content within the string is properly rendered, avoiding unexpected behavior or vulnerabilities.

## Key Differences

* `textContent`: Sets or gets the text content of a node, discarding any HTML tags.
* `innerHTML`: Sets or gets the HTML content of an element, allowing for the inclusion of HTML tags.

Using `innerHTML` is generally safer and more flexible when working with user input or dynamically generated HTML content, as it allows for proper rendering of HTML tags, while `textContent` is safer for static text that you know won't cause issues with unexpected behavior.  
