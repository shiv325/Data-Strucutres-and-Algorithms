# Algorithm Analysis

- Important part of computational complexity thory
- Provides theoritical estimation for required resources of algorithms to solve a problem
- Determination of amount of time and space resources required to execute a program

# Significance of Algorithm Analysis

- To predict behaviour of algorithm without implementing it on specific computer
- To have simple measures for algorithm efficiency instead of implementing and testing efficiency every time a certain parameter is changed
- Analysing different algorithms can help us compare them to determine the best algortihm

# Limitations of Algorithm Analysis

- It's impossible to predict exact behavior of algorithm as there are too many influencing factors
- Analysis is just an approximation; it's not perfect

# Types of Algorithm Analysis

1. Best Case
2. Worst Case
3. Average Case

### Best Case

- Input for which the algorithm takes minimum time
- Calculates lower bound of algorithm
- Example => In Linear Search, if the element to be found is present at index 0

### Worst Case

- Input for which algorithm takes maximum time
- Calculates upper bound of algorithm
- Example => In Linear Search, if the element to be found is not present

### Average Case

- Average Time to produce the result
- Takes all random inputs and calculates computation time for all inputs
- The Average Case is given by : $$\text{Average Case} = \frac{\text{Total Computation Time}}{\text{Total Number of Cases}}$$
