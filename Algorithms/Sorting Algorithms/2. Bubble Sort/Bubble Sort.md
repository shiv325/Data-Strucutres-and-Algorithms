# Bubble Sort

- Sorting Algorithm that sorts array from lowest to highest values
- Works by repeatedly swapping two numbers if they are in wrong order

## Algorithm

1. Go through the array, one at a time
2. For each value, compare it with the next value
3. If the value is greater than the next one, swap the values so that the highest value comes last
4. Go through the array till the second smallest number is sorted

## Manual Run Through

Given array A = {6, 3, 5, 0}

<table>
  <tr>
    <th>Element</th>
    <td>6</td>
    <td>3</td>
    <td>5</td>
    <td>0</td>
  </tr>
  <tr>
    <th>Index</th>
    <td>0</td>
    <td>1</td>
    <td>2</td>
    <td>3</td>
  </tr>
</table>

### __Passes__ :-

- Pass 1 :

    - Current Index = 0

        - Compare elements at indexes 0 and 1
        - 6 > 3
        - Swap them
    
          <table>
            <tr>
              <th>Element</th>
              <td>3</td>
              <td>6</td>
              <td>5</td>
              <td>0</td>
            </tr>
            <tr>
              <th>Index</th>
              <td>0</td>
              <td>1</td>
              <td>2</td>
              <td>3</td>
            </tr>
          </table>

    - Current Index = 1

        - Compare elements at indexes 1 and 2
        - 6 > 5
        - Swap them
    
          <table>
            <tr>
              <th>Element</th>
              <td>3</td>
              <td>5</td>
              <td>6</td>
              <td>0</td>
            </tr>
            <tr>
              <th>Index</th>
              <td>0</td>
              <td>1</td>
              <td>2</td>
              <td>3</td>
            </tr>
          </table>

    - Current Index = 2

        - Compare elements at indexes 2 and 3
        - 6 > 0
        - Swap them
    
          <table>
            <tr>
              <th>Element</th>
              <td>3</td>
              <td>5</td>
              <td>0</td>
              <td>6</td>
            </tr>
            <tr>
              <th>Index</th>
              <td>0</td>
              <td>1</td>
              <td>2</td>
              <td>3</td>
            </tr>
          </table>

- Pass 2 :

    - Current Index = 0

        - Compare elements at indexes 0 and 1
        - 3 < 5
        - Do nothing
    
          <table>
            <tr>
              <th>Element</th>
              <td>3</td>
              <td>5</td>
              <td>0</td>
              <td>6</td>
            </tr>
            <tr>
              <th>Index</th>
              <td>0</td>
              <td>1</td>
              <td>2</td>
              <td>3</td>
            </tr>
          </table>

    - Current Index = 1

        - Compare elements at indexes 1 and 2
        - 5 > 0
        - Swap them
    
          <table>
            <tr>
              <th>Element</th>
              <td>3</td>
              <td>0</td>
              <td>5</td>
              <td>6</td>
            </tr>
            <tr>
              <th>Index</th>
              <td>0</td>
              <td>1</td>
              <td>2</td>
              <td>3</td>
            </tr>
          </table>

- Pass 3 :

    - Current Index = 0

        - Compare elements at indexes 0 and 1
        - 3 < 0
        - Swap these
    
          <table>
            <tr>
              <th>Element</th>
              <td>0</td>
              <td>3</td>
              <td>5</td>
              <td>6</td>
            </tr>
            <tr>
              <th>Index</th>
              <td>0</td>
              <td>1</td>
              <td>2</td>
              <td>3</td>
            </tr>
          </table>

Finally, the array is sorted.

## Programs to Implement Bubble Sort

1. [Bubble Sort in Python]()
2. [Bubble Sort in C](https://github.com/shiv325/C/blob/dddced1838a8857f922a9168454e471d149f7b7b/Algorithms/Sorting%20Algorithms/Bubble%20Sort/Bubble%20Sort%20in%20C.c)
3. [Bubble Sort in C++]()
4. [Bubble Sort in Java]()
5. [Bubble Sort in JavaScript]()
