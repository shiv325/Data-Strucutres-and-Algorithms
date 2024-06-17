# Time Complexity

- Amount of time taken by algorithm to run as function of length of input
- It's not the actual execution time of machine on which algorithm is running on
- Considers how many times each statement is executed

# How to Calculate Time Complexity

    Total Time = Time(Statement1) + Time(Statement2) + ... + Time(StatementN)

Assume that

- n => Size of Input
- T(n) => Overall Time
- t => Amount of Time a statement or collection of statements takes to execute

We can say that

    T(n) = t(Statement1) + t(Statement2) + ... + t(StatementN)

# Types of Time Complexities

- Constant Time => O(1)
- Logarithmic Time => O(log n)
- Linear Time => O(n)
- Logarithmic-Linear Time => O(n*log n)
- Quadratic Time => O(n<sup>2</sup>)
- Bilinear Time => O(n*m)
- Cubic Time => O(n<sup>3</sup>)
- Exponential Time => O(2<sup>n</sup>)
- Factorial Time => O(n!)
- Polynomial Time => O(n<sup>k</sup>)

# Examples

- `Constant Time` :
    
          print("Hello World")
          a = 10
          b = 10
          c = a + b
          t = True

    - T(n) = t(Statement1) + t(Statement2) + t(Statement3) + t(Statement4) + t(Statement5)
    - Overall, T(n) = O(1)
    - We can assume that each statement takes constant time O(1)
    - So, time complexity is constant i.e. O(1)
    - Everytime, a constant amount of time is required to execute the code
    - Execution Time remains same regardless of input size
    - Examples => return, comparisons, assignments, reading variables, etc.

- `Logarithmic Time` :

      n = 16
      i = i
      while i <= n :
          print(i)
          i *= 2

    - T(n) = O(log<sub>2</sub> n)
    - Execution time logarithmically increases with input size
    - Examples => Binary Search
      

- `Linear Time` :

      for i in range(n) :
          print("Hello World")

    - 'Hello World' is printed _n_ times
    - Time taken to run this program is :

          T(n) = n * t(Print Statements)
               = n * O(1)
               = O(n)
    
    - Execution Time increases linearly with input size
    - Examples => Traversing arrays

- `Logarithmic Linear Time` :

      def merge_sort(arr):
        if len(arr) > 1:
            # Find the middle point and divide it
            mid = len(arr) // 2
            left_half = arr[:mid]
            right_half = arr[mid:]
    
            # Recursively sort the first half
            merge_sort(left_half)
            # Recursively sort the second half
            merge_sort(right_half)
    
            # Initialize indices for merging
            i = j = k = 0
    
            # Merge the sorted halves
            while i < len(left_half) and j < len(right_half):
                if left_half[i] < right_half[j]:
                    arr[k] = left_half[i]
                    i += 1
                else:
                    arr[k] = right_half[j]
                    j += 1
                k += 1
    
            # Check if any element was left
            while i < len(left_half):
                arr[k] = left_half[i]
                i += 1
                k += 1
    
            while j < len(right_half):
                arr[k] = right_half[j]
                j += 1
                k += 1

    - T(n) = O(n*log<sub>2</sub> n)
      
      - Division of Array :-
          
          - Each time, the array is divided into 2 sub-halves
          - Division process continues till each sub-array has only 1 element
          - No. of times we can divide array this way is log n
          - T(n) = O(log<sub>2</sub> n)

      - Merging of Sub-Arrays :-

          - Each level of recursion merges all elements once
          - For n elements in array, merging at each level involves O(n) operations
          - T(n) = O(n)

      - Calculation of Time Complexity :-
     
            Total time = t(Division) * t(Merging)
                       = O(log<sub>2</sub> n) * O(n)
                       = O(n*log<sub>2</sub> n)

    - Execution Time increases log-linearly with input size
    - Examples => Merge Sort

- `Quadratic Time` :

      d
