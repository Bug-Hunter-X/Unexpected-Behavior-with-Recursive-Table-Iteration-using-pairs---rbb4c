# Lua Table Iteration Bug

This repository demonstrates a subtle bug related to table iteration in Lua using the `pairs` iterator. The issue arises from the lack of guaranteed order in `pairs` and can lead to unexpected behavior when modifying the table during iteration, particularly in recursive scenarios.

## Bug Description
The `bug.lua` file contains a function that recursively iterates through a nested table.  The intended behavior is to traverse all nested tables. However, because `pairs` doesn't guarantee order, if the table is modified during the iteration, elements might be missed.

## Solution
The `bugSolution.lua` file provides a corrected version, using a safer iteration technique that avoids this problem. It demonstrates how to iterate using a sorted keys approach.