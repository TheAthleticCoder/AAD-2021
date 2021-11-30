# **Dynammic Programming**
### _**Main Focus:** Tiling Problem_
----

## **DP for Tiling Purposes:** 
Assume that we use dominoes measuring $2 \times 1$ to tile an infinite strip of height 2. How many ways can one tile a 2 $\times$ $n$ strip of square cells with 1 $\times$ 2 dominoes?

This is super relatable with respect to fitting things optimally in a suitcase or fitting bricks optimally on a wall and such. 



Notice that we can place tiles either vertically or horizontally. For placing vertical tiles, we need a gap
of at least 2 $\times$ 2. For placing horizontal tiles, we need a gap of 2 $\times$ 1. In this manner, the problem is reduced to finding the number of ways to partition $n$ using the numbers 1 and 2 with order considered relevant. 

*For example:* 11 = 1+2+2+1+2+2+1 (Seen in the above figure)

If we have to find such arrangements for 12, we can either place a 1 at the end or add 2 in the arrangements possible with 10. Similarly, let us say we have $F_n$, possible arrangements for $n$. Then for $(n+1)$, we can either place just 1 at the end or we can find possible arrangements for $(n-1)$ and put a 2 at the end. Using the above theory:

> $$F_{n+1} = F_n + F_{n-1}$$

Now, we verify the above theory and make it more self-explanatory:
1. In how many ways can we fill a 2 $\times$ 1 strip: 1 $\rightarrow$ Only 1 vertical tile.
2. In how many ways can we fill a 2 $\times$ 2 strip: 2 $\rightarrow$ Either 2 vertical tiles or 2 horizontal tiles. 
3. In how many ways can we fill a 2 $\times$ 3 strip: 3 $\rightarrow$ Either put 2 vertical tiles along with the 2 $\times$ 2 solution or 2 horizontal tiles along with the 2 $\times$ 3 solution. 
4. Similarly, now, how do we fill 2 $\times$ $n$ strip: Either put a vertical tile in the solutions possible for 2 $\times$ $(n-1)$ strip or put 2 horizontal tiles in the solution possible for a 2 $\times$ $(n-2)$ strip. [$F_{n-1}+F_{n-2}$]
5. The base case for the solution is: $F_1 = 1$ and $F_2 = 2$. 
-----
-----

