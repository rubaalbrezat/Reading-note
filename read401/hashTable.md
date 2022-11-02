# Hash Table

 hash table is an implementation of an associative array, a list of key-value pairs that allow you to retrieve a value via a key. Internally a hash table utilizes a hash function to transform a key value into an index that points to where the value is stored in memory. Hash tables have fast search, insertion and delete operations.

 The Hash table data structure stores elements in key-value pairs where

1. Key- unique integer that is used for indexing the values
2. Value - data that are associated with keys.

Hash Collision
When the hash function generates the same index for multiple keys, there will be a conflict (what value to be stored in that index). This is called a hash collision.


## Different techniques used in open addressing are:
i. Linear Probing
ii. Quadratic Probing
iii. Double hashing

## There are two main ways to implement a hash table/associative array in JavaScript:

1. Using the Object Data Type
2. Using a Map Object