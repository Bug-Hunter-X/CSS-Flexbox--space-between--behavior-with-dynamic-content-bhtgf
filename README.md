# CSS Flexbox `space-between` Behavior with Dynamic Content

This repository demonstrates a subtle bug related to the use of `justify-content: space-between` in CSS flexbox layouts when the number of flex items changes dynamically.  The issue arises because `space-between` distributes space *between* items, not around a single item.

## Problem

When using `justify-content: space-between` and the number of flex items reduces to one, that single item is placed at the beginning of the container, not centered as one might intuitively expect.

## Solution

The solution involves using a more robust approach that accounts for the number of items present.  See `bugSolution.css` for a better approach.

## How to Reproduce

1.  Clone this repository.
2.  Open `bug.html` in your web browser. Observe the layout.
3.  Comment out or remove one of the `.item` elements from the HTML.  Observe the change in the layout.