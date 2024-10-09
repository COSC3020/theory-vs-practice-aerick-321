# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.
  
1- Knowing the best case doesn't help find the average case

2- It can depend on the input/list size, one algorithm may be faster with smaller or already sorted lists that another but as the input grows it could switch

3- Two algorithms can have the same asymptotic analysis but the actual running time could be different

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.
  
It should take about 50 seconds because you have the traverse all the elements, O(n), so 10 times the elements would take 10 times as long.

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.



Add your answers to this markdown file.


Used geeksforgeeks.com to refresh on the time complexity of different operations in Binary search trees. “I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.”
