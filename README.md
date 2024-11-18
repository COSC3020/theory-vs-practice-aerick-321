# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.
  
1-The hardware and software can affect the performance because some machines may be more efficient with certain programs/algorithms than others. For example with quicksort on a machine with a faster CPU but slower memory, the algorithm may run faster when the list fits in the CPU cache. On another machine with slower disk access and smaller cache, the same quicksort might be slower with a larger list even though it still has the same asymptotic complexity.

2- Algorithms with higher asymptotic complexity might still perform better due to smaller constant factors or overhead in the algorithm. For example, if we compare two algorithms, one with time complexity 
𝑂(𝑛) and another with $𝑂(𝑛^3)$, the $𝑂(𝑛^3)$ algorithm might be faster for very small input sizes because its constant factors are smaller. However, as the input size grows, the difference in growth rates becomes bigger. The 
$𝑂(𝑛^3)$ algorithm will eventually become slower than the 𝑂(𝑛) algorithm because cubic growth outpaces linear growth as the input size increases. Constant factors are ignored once the input is large enough.

3- Two algorithms can have the same asymptotic analysis but the actual running time could be different. The asymptotic analysis only gives the general bounds so as n approaches infinity the runtimes could vary greatly even though they have the same expression. This is shown in the slides with the graph on slide 37 in sorting where quick sort and merge sort have the same average complexity O(nlogn) but their runtimes are vastly different. The aysmptotic expression doesn't tell you how the algorithm will actually work.

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.
  
The average case for Binary search tree is O(log(n)). For log2(1000) = 9.966 and for log2(10000) = 13.288. 13.288/9.966 = 1.333 growth rate. 1.333 x 5 = 6.665 seconds.

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

1- While using different compilers and languages can affect smaller inputs they can affect larger inputs even more because it takes longer to proccess to larger lists. If the two tests are run on different machines with one being less powerful it can significantly affect the time with the largers list that may need more memory and power to proccess.

2- It doesn't take in consideration of the type of element, the elements could have strings which would take longer to process than an integer.

3- The more elements there less that fit in the CPU's cache and that can cause more cache misses and memory swaps so there is slower access to the memory.


Add your answers to this markdown file.


Used geeksforgeeks.com to refresh on the time complexity of different operations in Binary search trees. The TA helped give me ideas for a thrid reason why the asymptotic complexity suggests a different time. “I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.”
