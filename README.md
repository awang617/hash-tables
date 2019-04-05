# Hash Tables
## Summary

![](https://upload.wikimedia.org/wikipedia/commons/thumb/7/7d/Hash_table_3_1_1_0_1_0_0_SP.svg/315px-Hash_table_3_1_1_0_1_0_0_SP.svg.png)

![](https://upload.wikimedia.org/wikipedia/commons/thumb/d/d0/Hash_table_5_0_1_1_1_1_1_LL.svg/450px-Hash_table_5_0_1_1_1_1_1_LL.svg.png)

## Examples

## Time Complexity
A good hash table will complete searching, inserting, and deleting in O(1) and spacing in O(n). The worst case scenario is when every insertion causes a hash collision and the table has to resort to a linear search, in which case the time commplexity becomes O(n). The speed of hash tables gives it a great advantage over other data structures. However, when the size of data is not very large, hash tables become higher cost to implement.

## Collision Resolution
Open Hashing - Allow multiple values to exist on the same index by creating a linked list.
https://www.cs.usfca.edu/~galles/visualization/OpenHash.html

Closed Hashing - If the  index is already occupied, find another open index to store the value.
Common approaches: Linear Probing, Quadratic Probing, and Double Hashing examples here:
https://www.cs.usfca.edu/~galles/visualization/ClosedHash.html

  Linear Probing - Move +1 index until an open slot is available, short time to process but it can create clusters.

  Quadratic Probing - Better spacing of indexes by you squaring the incremented value.
    If slot hash(x) % S is full, then we try (hash(x) + 1*1) % S
    If (hash(x) + 1*1) % S is also full, then we try (hash(x) + 2*2) % S
    If (hash(x) + 2*2) % S is also full, then we try (hash(x) + 3*3) % S

  Double Hashing - Rehash
    If slot hash(x) % S is full, then we try (hash(x) + 1*hash2(x)) % S
    If (hash(x) + 1*hash2(x)) % S is also full, then we try (hash(x) + 2*hash2(x)) % S
    If (hash(x) + 2*hash2(x)) % S is also full, then we try (hash(x) + 3*hash2(x)) % S

## Common Interview Questions
Given an array of numbers, find two pairs that sum to the same amount.
https://www.geeksforgeeks.org/find-four-elements-a-b-c-and-d-in-an-array-such-that-ab-cd/

### Other Resources
https://www.youtube.com/watch?v=KyUTuwz_b7Q
