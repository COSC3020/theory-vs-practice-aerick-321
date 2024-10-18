# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.
  
1- Knowing the best case doesn't help find the average case, they are not always the same. Average case inputs are often not the ideal inputs you get with the best case. The average case is the practical everyday use and not the perfect ideal input that can be misleading with the fast time.

2- It can depend on the input/list size, one algorithm may be faster with smaller list but as the input grows it could switch for example 90000n is slower with a smaller list and n^3 is slower with a larger list

3- Two algorithms can have the same asymptotic analysis but the actual running time could be different

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.
  
The average case for Binary search tree is O(log(n)). For log2(1000) = 9.966 and for log2(10000) = 13.288. 13.288/9.966 = 1.333 growth rate. 1.333 x 5 = 6.665 seconds.

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

1- The input could be close to the worst case which is O(n) and almost a list even though it is technically still the avaerage case and that can cause a longer time

2- Different compilers like c++ can cause different optimization in places or not optimize certain loops.

3- The more elements there less that fit in the CPU's cache and that can cause more cache misses and memory swaps so there is slower access to the memory.


Add your answers to this markdown file.


Used geeksforgeeks.com to refresh on the time complexity of different operations in Binary search trees. The TA helped give me ideas for a thrid reason why the asymptotic complexity suggests a different time. “I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.”
