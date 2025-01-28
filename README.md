# JavaScript Loose Comparison Bug

This repository demonstrates a common yet subtle bug in JavaScript related to loose comparison and type coercion. The `foo` function aims to handle null, negative numbers, and positive numbers differently. However, a loose comparison (`==`) may produce unexpected results when `x` is not explicitly null, but rather `undefined` or another falsy value.

## Bug Description
The issue lies in how JavaScript handles loose comparison.  The `if (x === null)` part is only true for null values. Other falsy values, such as `0`, `""`, or `false`, will be incorrectly handled. 

## Solution
The solution involves using strict comparison (`===`) or explicitly checking for specific falsy values (or better yet, using a more robust and explicit logic).