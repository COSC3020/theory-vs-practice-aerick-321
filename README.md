# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.
  
1-The hardware and software can affect the performance because some machines may be more efficient with certain programs/algorithms than others. For example with quicksort on a machine with a faster CPU but slower memory, the algorithm may run faster when the list fits in the CPU cache. On another machine with slower disk access and smaller cache, the same quicksort might be slower with a larger list even though it still has the same asymptotic complexity.

2- Algorithms with higher asymptotic complexity might still perform better due to smaller constant factors or overhead in the algorithm. For example, if we compare two algorithms, one with time complexity 
𝑂(𝑛) and another with $𝑂(𝑛^3)$, the $𝑂(𝑛^3)$ algorithm might be faster for very small input sizes because its constant factors are smaller. However, as the input size grows, the difference in growth rates becomes bigger. The 
$𝑂(𝑛^3)$ algorithm will eventually become slower than the 𝑂(𝑛) algorithm because cubic growth outpaces linear growth as the input size increases. Constant factors are ignored once the input is large enough.

3-Performance can also depend on the compiler or interpreter used for a programming language. For instance, C++ compilers are highly optimized to produce efficient machine code, enabling better utilization of system resources. This makes C++ programs generally faster in execution compared to Python.

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.
  
The average case for Binary search tree is O(log(n)). For log2(1000) = 9.966 and for log2(10000) = 13.288. 13.288/9.966 = 1.333 growth rate. 1.333 x 5 = 6.665 seconds.

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

1- While using different compilers and languages can affect smaller inputs they can affect larger inputs even more because it takes longer to proccess to larger lists. If the two tests are run on different machines with one being less powerful it can significantly affect the time with the largers list that may need more memory and power to proccess.

2- Disk memory can also affect the time and slow it down because it needs frequent I/O if data exceeds RAM capacity. Getting data from disk is much slower than getting it from main memory (RAM). When the data structure can't fit into RAM and parts of it must be stored on disk, operations that require frequent access to this data will experience significant delays.

3- The more elements there less that fit in the CPU's cache and that can cause more cache misses and memory swaps so there is slower access to the memory.


Add your answers to this markdown file.


Used geeksforgeeks.com to refresh on the time complexity of different operations in Binary search trees. The TA helped give me ideas for a third reason why the asymptotic complexity suggests a different time, a third reason why asymptotic analysis can be misleading, and he gave me the idea to use disk memory as a reason. Used chat gpt to explain my 3rd reason in the 3rd question better. “I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.”
