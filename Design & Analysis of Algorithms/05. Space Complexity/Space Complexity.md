# Space Complexity

- Total Space taken by algorithm with respect to input size
- Required amount of memory to solve given problem

# Auxiliary Space

- Extra or temporary space taken by algorithm to complete the task

# Estimation of Memory Requirement

- Memory is divided into 2 parts :

  1. `Fixed Part` :

    - Independent of input size
    - Includes memory for instructions, constants, variables, etc.

  2. `Variable Part` :

    - Dependent on input size
    - Includes memory for recursion stack, referenced variables, etc.

# Examples

-     int add (int n){
        if (n <= 0){
          return 0;
        }
        return n + add (n-1);
      }

  - This function recursively calls itself
  - Calculates add(n), add(n - 1), add(n - 2), ..., add(2), add(1), add(0)
  - 
