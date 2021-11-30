# **Divide And Conquer**
### _**Main Focus:** Closest Pair of Points_
----

### **NOTE:** See Video To Understand This Well!
 
**$O(nlogn)$ solution:** Divide the points into 2 equal halves based on median of $x$- coordinates. 

**Algorithm:** 
1. Sort the given points in $S$ (given set of points) based on their $x$-coordinates. Partition $S$ into two subsets $S_1$ and $S_2$, about the line $l$ through median os $S$. $\leftarrow$ Divide Part of DnC.

2. Find the closest-pairs in $S_1$ and $S_2$ and call them $L$ and $R$ recursively.

3. Now, steps 4 to 8 form the Combining component of the DnC technique.

4. Let us assume that $\delta$ = $min(L,R)$.

5. Eliminate points that are farther than $\delta$ apart from $l$.

6. Consider the remaining points and sort based on their $y$-coordinates. 

7. Scan the remaining points in the $y$ order and compute the distances of each point to all its neighbours that are distanced no more than $2 \times \delta$ (that's the reason for sorting according to $y$)-

8. If any of these distances is less than $\delta$ then update $\delta$.

**Analysis:**
1. Step 1 and 2 take $O(nlogn) for sorting and recursively finding the minimum.$
2. Step 4 takes $O(1)$.
3. Step 5 takes $O(n)$ for scanning and elimination.
4. Step 6 takes $O(nlogn)$ for sorting.
5. Step 7 takes $O(n)$ for scanning. 

**Therefore, Total Compexity: $O(nlogn)+O(1)+O(n)+O(n)+O(n) \approx O(nlogn)$**

Images Used In The Video:

-----
-----

