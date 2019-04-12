# 60_wrapBinarySearch

0. Problem: Given an ArrayList of n String items, return the index of a given String item

1. Recursive Abstraction: When I am asked to return the index of a String item in an ArrayList with an index range of n, then the recursive abstraction can return the index of the String item in an ArrayList with an index range of n / 2 using the same directions

2. Solution to the Base Case:
    - if the lower bound is ever less than the upper bound, then return an error ( -2)
    - if the lexiographic value for the given String item is equal to the value of the item on the current page, then return the index of that page
    
    Binary Decision:
      - is the lexiographic value for the given String item equal to the value of the item on the current page
    
    Solution to the Recursive Case:
    
    Additional Processing is not needed
    Combiner Element is not needed
    
    Recursive Abstraction:
      - if the lexiographic calue for the given String item is less than the value of the item on the current page, then ask the recursive abstraction to find the index of the given String item with:
        - the lower bound as the lower bound
        - the upper bound as the current page
        - the current page as the average between the original upper bound and lower bound
      using these instructions
      
      - if the lexiographic calue for the given String item is greater than the value of the item on the current page, then ask the recursive abstraction to find the index of the given String item with:
        - the lower bound as the current page
        - the upper bound as the upper bound
        - the current page as the average between the original upper bound and lower bound
       using these instructions
