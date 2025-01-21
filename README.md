# CSS `calc()` and `attr()` Incompatibility

This repository demonstrates an uncommon bug related to the interaction between the CSS `calc()` function and the `attr()` function.  The issue arises from attempting to perform a calculation involving a dynamically retrieved attribute value and units within `calc()`.  The provided solution offers a workaround.

## Bug Description

The original CSS code attempts to calculate the width of an element based on a data attribute (`data-width`) using the `calc()` function.  However, because `attr()` returns a string, multiplying it directly by `1px` within `calc()` results in unexpected behavior or an error, depending on the browser's handling of this edge case. 

## Solution

The solution uses a more robust approach by converting the `attr()` value to a number and explicitly specifying the unit in the `calc()` function.