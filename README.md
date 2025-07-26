# Leetcode-2652.-Sum-Multiples
# Description
Given a positive integer n, find the sum of all integers in the range [1, n] inclusive that are divisible by 3, 5, or 7.

Return an integer denoting the sum of all numbers in the given range satisfying the constraint.
# Solution
In the given problem we have been given an integer number num , we have to find the sum of all numbers which are divisible by either 3 , 5 or 7 in the range [1,n].

Example :

n=7

Numbers in the range [1, 7] that are divisible by 3, 5, or 7 are 3, 5, 6, 7. The sum of these numbers is 21.

# Algorithm
1. Create an empty array named as result , in which we will be storing the numbers which are divisible by 3,5 or 7.
2. Use a for loop which loops from the range [1,n+1]
3. Check if the number is divisible by 3,5 or 7. If it is divisible then append it to the array.
4. Return the sum of the array.

# Code
class Solution:

    def sumOfMultiples(self, n: int) -> int:
        result=[]
        for i in range(1,n+1):
            if i %3==0 or i%5==0 or i%7==0:
                result.append(i)
        return sum(result)
# Time Complexity
for i in range(1, n + 1) → runs n times → O(n)

Inside the loop:

% (modulus) operations and logical comparisons are constant time → O(1)

result.append(i) may occasionally happen but still in constant time → O(1) per append

Hence, overall time complexity:
O(n)
