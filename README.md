Galactic Cargo Management System (GCMS)
The Galactic Cargo Management System (GCMS) is designed to tackle the challenge of efficiently packing cargo bins in an interstellar shipping environment. The system manages bins and cargo objects, each with a unique ID, and handles the allocation of cargo based on color-specific algorithms.

Features
Bin Management: Add cargo bins with a specified capacity and unique ID.
Object Management: Add objects with varying sizes and colors, and assign them to the appropriate bin based on the cargo type and packing algorithm.

Color-Specific Algorithms:
Blue Cargo (Compact Fit, Least ID): Assigns to the smallest bin that can accommodate the cargo, prioritizing bins with the least ID.
Yellow Cargo (Compact Fit, Greatest ID): Similar to Blue Cargo, but chooses bins with the greatest ID in case of a tie.
Red Cargo (Largest Fit, Least ID): Assigns to the bin with the largest remaining capacity, prioritizing bins with the least ID.
Green Cargo (Largest Fit, Greatest ID): Similar to Red Cargo, but chooses bins with the greatest ID in case of a tie.
Efficient Object Deletion: Objects can be removed from their assigned bins, updating bin capacities accordingly.
Info Functions: Retrieve detailed information about bins and objects, including bin capacity and objects assigned.

Time Complexity
Operations like adding/removing objects and bins are optimized with AVL trees, ensuring a time complexity of O(log n) for most operations.

Requirements
No use of Python dictionaries or sets.

Space complexity: O(n + m), where n is the number of bins and m is the number of objects.

Exception handling for cases when no suitable bin is found.


Files
gcms.py: Main logic for the GCMS class.
bin.py: Defines the Bin class.
object.py: Defines the Object class.
avl.py: AVL tree implementation used for efficient lookups.
node.py: Defines nodes for the AVL trees.
exceptions.py: Handles custom exceptions (unmodified).
main.py: For debugging purposes.


Installation
Clone the repository and run main.py to test the system.
