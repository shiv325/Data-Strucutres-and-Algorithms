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

|                Type                |     Notation     |
| :--------------------------------: | :--------------: |
|           Constant Time            |        O(1)      |
|         Logarithmic Time           |      O(log n)    |
|            Linear Time             |        O(n)      |
| Logarithmic-Linear or Super Linear |     O(n log n)   |
|           Quadratic Time           | O(n<sup>2</sup>) |
|            Bilinear Time           |       O(n*m)     |
|              Cubic Time            | O(n<sup>3</sup>) |
|          Exponential Time          | O(2<sup>n</sup>) |
|           Factorial Time           |       O(n!)      |
|           Polynomial Time          | O(n<sup>k</sup>) |

> ___Note*___ : These time complexities are ordered from lowest to highest as we move from top to bottom

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
    - Examples => Binary Search, etc.
      

- `Linear Time` :

      for i in range(n) :
          print("Hello World")

    - 'Hello World' is printed _n_ times
    - Time taken to run this program is :

          T(n) = n * t(Print Statements)
               = n * O(1)
               = O(n)
    
    - Execution Time increases linearly with input size
    - Examples => Traversing arrays, Finding Maximum or Minimum in Arrays, etc.

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
    - Examples => Merge Sort, etc.

- `Quadratic Time` :

      for i in range(n) :
          for j in range(n) :
              print(i, j)

    - T(n) = O(n<sup>2</sup>)
    - For each outer loop iteration, the inner loop iterates 'n' times
    - Calculation of Time Complexity :-
     
            Total time = t(Outer Loop Iteration) * t(Inner Loop Iteration)
                       = O(n) * O(n)
                       = O(n<sup>2</sup>)

    - Execution Time is roughly proportional to square of input size
    - Examples => Bubble Sort, Selection Sort, Nested Loops, Insertion Sort, etc.

- `Bilinear Time` :

      for i in range(n) :
          for j in range(m) :
              print(i * j)

    - T(n) = O(n*m)
    - For each outer loop iteration, the inner loop iterates 'm' times
    - Calculation of Time Complexity :-
     
            Total time = t(Outer Loop Iteration) * t(Inner Loop Iteration)
                       = O(n) * O(m)
                       = O(n*m)
 
    - Execution time depends on both the input sizes 'n' and 'm' linearly
    - Overall, the time complexity evaluates to O(n<sup>2</sup>)
    - Examples => Operation on Matrices, etc.

- `Cubic Time` :

      for i in range(n) :
          for j in range(n) :
              for k in range(n) :
                  print(x, y, z)

    - T(n) = O(n<sup>3</sup>)
    - For each outermost loop iteration, the middle inner loop iterates 'n' times
    - For each first middle inner loop, the inner most loop iterates 'n' times
    - Calculation of Time Complexity :-
     
            Total time = t(Outer Most Loop Iteration) * t(Middle Inner Loop Iteration) * t(Inner Most Loop Iteration)
                       = O(n) * O(n) * O(n)
                       = O(n<sup>3</sup>)
 
    - Execution time is directly proportional to cube of input size
    - Examples => Naive Matrix Multiplication, Processing all possible triplets in a set, etc.

- `Exponential Time` :

      def fibonacci(n) :
          if n <= 1 :
              return n
          return fibonacci(n - 1) + fibonacci(n - 2)

    - T(n) = O(2<sup>n</sup>)
    - For each call to fibonacci(n), 2 more calls are made i.e. fibonacci(n - 1) and fibonacci(n - 2)
    - Therefore, each function call results into calling of 2 more function calls
    - This results in exponential increase in function calls i.e. 2<sup>n</sup>
    - Execution Time increases exponentially with input size
    - Examples => Finding Power Set(Set of Subsets), Fibonacci Series, Towers of Hanoi, etc.

- `Factorial Time` :

      def generate_permutations(s):
          if len(s) == 1:
              return [s]
        
          perms = []
          for i, char in enumerate(s):
              remaining = s[:i] + s[i+1:]
              for perm in generate_permutations(remaining):
                  perms.append(char + perm)
          return perms

    - T(n) = O(n!)
    - For 'n' elements, there are 'n' choices for 1st element, (n - 1) choices for 2nd element, (n - 2) choices for 3rd element, and so on
    - Total number of permutations = n × (n - 1) × (n - 2) × ... × 3 × 2 × 1 = n!
    - Execution Time increases rapidly with input size
    - Examples => Solving n-queens problem, Finding all possible permutations, etc.

- `Polynomial Time` :

    - T(n) = O(n<sup>k</sup>)
    - Here, 'k' can be any constant number
    - Even for small inputs, the time time complexity can be extremely high
    - Execution Time is proportional to n<sup>k</sup>
    - Examples of Complexites => O(n), O(n<sup>2</sup>), O(n<sup>3</sup>), O(n<sup>4</sup>), O(n<sup>5</sup>), and so on

# Graphs of Time Complexities

![Time Complexities](https://github.com/shiv325/Data-Strucutres-and-Algorithms/blob/5e2fc0f47b38f2144a19b85405a516f683093199/Resources/time-complexity.jpg)

# Time Complexity of Popular Algorithms

|       <h2>Algorithm</h3>         | <h2>Best Time Complexity</h2> | <h2>Average Time Complexity</h2> | <h2>Worst Time Complexity</h2> |
| :------------------------------: | :---------------------------: | :------------------------------: | :----------------------------: |
|   <h3>Sorting Algorithms</h3>    |                               |                                  |                                |
|          Bubble Sort             |             O(n)              |             O(n^2)               |             O(n^2)             |
|         Selection Sort           |            O(n^2)             |             O(n^2)               |             O(n^2)             |
|        Insertion Sort            |             O(n)              |             O(n^2)               |             O(n^2)             |
|           Merge Sort             |          O(n log n)           |           O(n log n)             |           O(n log n)           |
|           Quick Sort             |          O(n log n)           |           O(n log n)             |             O(n^2)             |
|            Heap Sort             |          O(n log n)           |           O(n log n)             |           O(n log n)           |
|         Counting Sort            |           O(n + k)            |            O(n + k)              |            O(n + k)            |
|           Radix Sort             |            O(nk)              |             O(nk)                |              O(nk)             |
|          Bucket Sort             |           O(n + k)            |            O(n + k)              |             O(n^2)             |
| ******************************** | ***************************** | ******************************** | ****************************** |
|  <h3>Searching Algorithms</h3>   |                               |                                  |                                |
|         Linear Search            |            O(1)               |              O(n)                |              O(n)              |
|         Binary Search            |            O(1)               |            O(log n)              |            O(log n)            |
| ******************************** | ***************************** | ******************************** | ****************************** |
|    <h3>Graph Algorithms</h3>     |                               |                                  |                                |
|     Depth-First Search (DFS)     |           O(V + E)            |            O(V + E)              |            O(V + E)            |
|    Breadth-First Search (BFS)    |           O(V + E)            |            O(V + E)              |            O(V + E)            |
|      Dijkstra’s Algorithm        |        O(E + V log V)         |         O(E + V log V)           |          O(E + V log V)        |
|      Bellman-Ford Algorithm      |            O(VE)              |             O(VE)                |              O(VE)             |
|     Floyd-Warshall Algorithm     |            O(V^3)             |             O(V^3)               |              O(V^3)            |
| ******************************** | ***************************** | ******************************** | ****************************** |
|   <h3>Dynamic Programming</h3>   |                               |                                  |                                |
|     Fibonacci Sequence (DP)      |             O(n)              |              O(n)                |               O(n)             |
| Longest Common Subsequence (LCS) |            O(mn)              |              O(mn)               |               O(mn)            |

# Comparing Algorithms

- `Execution Times` :
    - Not a good measure
    - It's specific to a particular computer

- `No. of Statements Executed` :
    - Not a good measure
    - Varies with programming language and style of individual programmer

So, ideal solution is =>

- Assume that running time of given algorithm is function of input size 'n' i.e. f(n)
- Compare different algorithms corresponding to different runtime
- This comparison is independent of machine time, programming style, etc.
