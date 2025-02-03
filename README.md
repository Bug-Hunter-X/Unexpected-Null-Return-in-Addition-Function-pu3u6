# Unexpected Null Return in Addition Function

This repository demonstrates a subtle bug in a JavaScript addition function. The function is designed to handle null values gracefully, but it unexpectedly returns null even when one of the inputs is zero, which is a falsy value but not necessarily a null value.

## Bug Description

The `foo` function checks if either input `a` or `b` is strictly equal to `null`. If either is `null`, it returns `null`. However, this behavior is problematic because 0 (zero) is considered a falsy value in JavaScript. This might lead to unintended null returns when a or b is 0, which is a perfectly valid number. 

## Solution

The solution addresses the issue by explicitly checking for null and undefined instead of using loose equality checks that may treat 0 as a falsy value.