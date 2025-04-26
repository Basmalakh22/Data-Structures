# Complexity

- Complexity in data structures is a fundamental concept in computer science that helps us analyze the performance and efficiency of algorithms. It allows us to quantify the resources (such as `time and memory`) required by an algorithm to solve a problem as the input size grows.

- Base Case (Omega notation  `Ω`): Often denoted by `O(1)` which signifies constant time, independent of input size.
- Average Case (Theta notation  `Θ`): inear search has an average case of `O(n/2)`, meaning it takes half the comparisons, on average, to find an element in a list.
- Worst Case (Big O notation `O`): Linear search’s worst case is `O(n)`, signifying it may need to compare all elements if the target is not present or at the end.

## From Best To Worst

- O(1) --> O(log n) --> O(n) --> O(n log n) --> O(n^2) --> O(2^n) --> O(n!)
