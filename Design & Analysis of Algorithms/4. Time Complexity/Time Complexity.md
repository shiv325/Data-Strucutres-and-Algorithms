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

- Constant Complexity O(1)
- Linear Complexity O(n)
- 

# Examples

- `Basic Statements` :

    - Examples => return, comparisons, assignments, reading variables, etc.
    
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

- `Loops` :

      for i in range(n) :
          print("Hello World")

    - 'Hello World' is printed _n_ times
    - Time taken to run this program is :

          T(n) = n * t(Print Statements)
               = n * O(1)
               = O(n)
    
    - 
