# Asymptotic Analysis

- Evaluates performance of algorithm in terms of input size
- Describes running time or space complexities based on input size
- Doesn't measures the actual running time
- Calculates how time or space taken by algorithm increases with input size
- Measures efficiency of algorithms that don't depend on machine-specific constants
- Need not implement algorithms to compare them
- Focuses on relative growth rates of algorithm's complexities

# Asymptotic Notations

- Way to describe running time or space complexities based on input size
- Mathematical tools to represent time complexity of algorithms
- Analyse performance of algorithms by understanding change in efficiency with respect to change in input size
- Concisely expresses behaviour of algorithm's time or space complexity as input size approaches infinity
- Enables comparison of algorithms' efficiency by abstracting away machine-specific constants and implementation details
- Focuses on fundamental trends

# Types of Asymptotic Notations

- Big-O (O) Notation
- Omega (Ω) Notation
- Theta (Θ) Notation
- Little-O (o) Notation
- Little-Omega (ω) Notation

# Properties of Asymtotic Notation

1. `General Properties` :

    - If f(n) is O(g(n)), then a*f(n) is also O(g(n)), where a is a constant
    - If f(n) is Θ(g(n)), then a * f(n) is also Θ(g(n)), where a is a constant
    - If f(n) is Ω (g(n)), then a * f(n) is also Ω (g(n)), where a is a constant

    Example =>
  
       f(n) = 2n²+5 is O(n²) 
       Then,
       7*f(n) = 7(2n²+5)
              = 14n²+35 is also O(n²)

2. `Transitive Properties` :

    - If f(n) is O(g(n)) and g(n) is O(h(n)), then f(n) = O(h(n))
    - If f(n) is Θ(g(n)) and g(n) is Θ(h(n)), then f(n) = Θ(h(n))
    - If f(n) is Ω (g(n)) and g(n) is Ω (h(n)), then f(n) = Ω (h(n))

    Example =>
    
       If f(n) = n, g(n) = n², h(n)=n³
       Then,
       n is O(n²) and n² is O(n³) then, n is O(n³)

3. `Reflexive Properties` :

    - Maximum value of f(n) will be f(n) itself
    - If f(n) is given, then f(n) is O(f(n))
    - If f(n) is given, then f(n) is Θ(f(n))
    - If f(n) is given, then f(n) is Ω (f(n))
    - f(n) and O(f(n) tie themselves in reflexive relation always

    Example =>

       f(n) = n²
       Then,
       f(n) is O(n²) i.e O(f(n)) 

4. `Symmetric Properties` :

    - If f(n) is Θ(g(n)), then g(n) is Θ(f(n))

    Example =>

       If(n) = n² and g(n) = n²
       Then,
       f(n) = Θ(n²) and g(n) = Θ(n²)

> _Note*_ : This property only satisfies for Θ notation

5. `Transpose Symmetric Properties` :

    - If f(n) is O(g(n)), then g(n) is Ω (f(n))

    Example =>

       If f(n) = n , g(n) = n²
       Then,
       n is O(n²) and n² is Ω (n)

> _Note*_ : This property only satisfies for O and Ω notation

6. `Some More Properties` :

     - If f(n) = O(g(n)) and f(n) = Ω(g(n)), then f(n) = Θ(g(n))
     - If f(n) = O(g(n)) and d(n)= O(e(n)), then f(n) + d(n) = O(max(g(n), e(n)))
     - If f(n)= O(g(n)) and d(n) = O(e(n)), then f(n) * d(n) = O(g(n) * e(n))

    Examples =>

      -     f(n) = n i.e O(n) 
            d(n) = n² i.e O(n²) 
            Then,
            f(n) + d(n) = n + n² i.e O(n²)

      -     f(n) = n i.e O(n) 
            d(n) = n² i.e O(n²)
            Then,
            f(n) * d(n) = n * n² = n³ i.e O(n³)
