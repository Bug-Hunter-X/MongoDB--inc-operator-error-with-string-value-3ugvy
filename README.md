# MongoDB $inc operator error with string value

This repository demonstrates a common error when using the `$inc` operator in MongoDB update queries.  The error arises from providing a string value to the `$inc` operator instead of a number, leading to unexpected behavior or errors.

## Bug Description
The `$inc` operator is used to increment a numerical field in a MongoDB document. However, if a string value is passed to `$inc`, it results in unexpected behavior and errors. The update query might fail or produce incorrect results.

## Solution
The solution involves ensuring that the value passed to the `$inc` operator is a number. This can be achieved by using numerical values or converting strings to numbers before using them with `$inc`.

## How to reproduce the bug
1.  Set up a MongoDB instance.
2.  Create a collection called `myCollection` with a document that has a numerical field `count`.
3.  Execute the buggy code in `bug.js`.
4. Observe the error or unexpected result.

## How to fix the bug
1. Replace the string value used with `$inc` with a numerical value.
2. Alternatively, convert string values to numbers using the `parseInt()` function before passing them to `$inc`.