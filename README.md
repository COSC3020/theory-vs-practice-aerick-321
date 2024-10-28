# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.
  
1- Asymptotic analysis normally focuses on the worst-case or even the average-case complexity. In practice, many algorithms perform much better on average than their worst-case complexity suggests. Like with quicksort's best and average case
is O(nlogn) while the worst case is $O(n^2)$.

2- Algorithms with higher asymptotic complexity might still perform better due to smaller constant factors or overhead in the algorithm. For example, if we compare two algorithms, one with time complexity 
𝑂(𝑛) and another with $𝑂(𝑛^3)$, the $𝑂(𝑛^3)$ algorithm might be faster for very small input sizes because its constant factors are smaller. However, as the input size grows, the difference in growth rates becomes bigger. The 
$𝑂(𝑛^3)$ algorithm will eventually become slower than the 𝑂(𝑛) algorithm because cubic growth outpaces linear growth as the input size increases. Constant factors are ignored once the input is large enough.

3- Two algorithms can have the same asymptotic analysis but the actual running time could be different. the complexity is O(nlogn) for both QuickSort and MergeSort and ignores constant factors and lower-order terms. However, these constants can make one algorithm significantly faster than another for the same input size, even if they share the same growth rate. For instance, QuickSort often has a smaller constant factor than MergeSort, making it faster in practice despite both being 𝑂(𝑛log𝑛) on average.

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.
  
The average case for Binary search tree is O(log(n)). For log2(1000) = 9.966 and for log2(10000) = 13.288. 13.288/9.966 = 1.333 growth rate. 1.333 x 5 = 6.665 seconds.

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

1- The way nodes are structured in memory, the pointers between nodes, might not be optimized. As the tree grows, inefficiencies in how memory is allocated and how pointers are followed could cause slowdowns. With a 10,000-element tree, ineffective memory layouts might lead to greater traversal times, even though the asymptotic complexity remains O(logn).

2- It doesn't take in consideration of the type of element, the elements could have strings which would take longer to process than an integer.

3- The more elements there less that fit in the CPU's cache and that can cause more cache misses and memory swaps so there is slower access to the memory.


Add your answers to this markdown file.


Used geeksforgeeks.com to refresh on the time complexity of different operations in Binary search trees. The TA helped give me ideas for a thrid reason why the asymptotic complexity suggests a different time. Chat gpt helped me explain some of my answers better. “I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.”
