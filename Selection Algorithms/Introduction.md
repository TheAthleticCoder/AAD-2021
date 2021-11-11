# **Selection Algorithms**
### _**Main Focus:** Introduction_
----

## **Understanding Selection Algorithms**
It is an algorithm used for finding the $k^{th}$ smallest or the largest number in a list. There are multiple solutions which provide different complexities and we shall try to cover those. 

## **Selection by Sorting**
We can convert a selection problem into a sorting problem and solution. We sort the input elements and then obtain the desired results based on our wants. 

If we want to get the $k^{th}$ smallest element, we just need to sort the list of elements and and scan and find the element present in that $k^{th}$ index. 

When we try to formulate the time complexity of the above procedure, we realise that this method requires $O(nlogn)$ time for sorting purposes ($n$ is length of the input list). If we perform $n$ queries, then the average cost per operation is $nlogn/n \approx O(nlogn)$. 

-----
-----

