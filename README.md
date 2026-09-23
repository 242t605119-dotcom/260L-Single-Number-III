# Single Number III

**LeetCode Problem:** 260
**Language:** Python

## Problem

Given an integer array `nums` where every number appears exactly twice except for two numbers that appear only once, find the two numbers that appear only once.

The answer can be returned in any order.

## Example

Input:

```text
nums = [1, 2, 1, 3, 2, 5]
```

The numbers `1` and `2` appear twice.

The numbers `3` and `5` appear only once.

Output:

```text
[3, 5]
```

## Approach

This solution uses the XOR operation.

First, XOR all the numbers in the array.

Since:

```text
a ^ a = 0
```

numbers that appear twice cancel each other.

The remaining result is the XOR of the two numbers that appear only once.

Next, we find a bit where these two numbers are different. This allows us to divide the numbers into two groups.

One group contains one of the unique numbers, and the other group contains the second unique number.

We then XOR the numbers in each group separately to find the two answers.

## Key Idea

The important XOR properties are:

```text
a ^ a = 0
a ^ 0 = a
```

Because duplicate numbers cancel each other, XOR is useful for finding numbers that occur only once.

## Complexity

* **Time:** O(n)
* **Space:** O(1)

The array is scanned twice, and only a few extra variables are used.

## Key Learning

This problem helped me practice:

* XOR operation
* Bit manipulation
* Array traversal
* Finding unique elements
* Using bit properties to optimize a solution

## Conclusion

The solution uses XOR and bit manipulation to find the two numbers that appear only once. It avoids using extra data structures and works efficiently in linear time.

**Author: T. Nandhini**
