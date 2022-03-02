# Binary Search Algorithm (Half interval search)
---
- Searching algorithm used in ==sorted arrays ONLY==
- Divide and Conquer
- In an iteration, half of the elements are eliminated
- Efficient for large arrays, ideal when ==resorting is not required==

1. Compare search value with value in the middle of array
	1. If values match, value is found
	2. If search value smaller than middle element, repeat action in the sub array to the left of the middle element
	3. If search value bigger than middle element, repeat action in sub array to the right of the middle element
2. If remaining array to be searched is empty, value was not found

Binary search vs [[Sequential Search]]
![[Binary Search vs sequential search.png]]