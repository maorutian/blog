---
title: Leetcode Two Sum in Javascript
date: 2020-04-30 21:15:24
categories: 
- Leetcode
tags:
- Javascript
- Leetcode
- Map
- Hash Table
---
Question [Leetcode - Two Sum](https://leetcode.com/problems/two-sum/)

```
Given an array of integers, 
return indices of the two numbers such that they add up to a specific target.
You may assume that each input would have exactly one solution, 
and you may not use the same element twice.
```

<!-- more -->

## 1.Brute Force

### Thought

1. Loop1: Loop through each element  num[i]
2. Loop2: In Loop1, Loop through the other elements num[j] in Loop1
3. In Loop2, If num[j] is equal to target minus num[i], return i and j

### Code

```
var twoSum = function (nums, target) {
      for (let i = 0; i < nums.length; i++) {
        for (let j = i + 1; j < nums.length; j++) {
          if (nums[j] === target - nums[i]) {
            return [i, j]
          }
        }
      }
```

### Complexity Analysis

* Time complexity : `O(n^2)` For each element, we try to find its complement by looping through the rest of array which takes O(n)O(n) time.
* Space complexity : `O(1)`.

## 2.Hash Table

### Thought

1. Create a Map
2. Loop1: Loop through each element num[i]
3. In Loop1: Caculate target  minus num[i], assume answer is x
4. If x is not in the map, set x as key and i as value in the map  
   If x already exists in the map, return num[i] and the value of x
5. return empty array if Loop1 doesn't return anything

#### Why we use Map? Can we use Object?

Yes, We can use `Object` as our Hash Table, because both store key-value pairs. But 
`Map` is mainly used for fast searching and looking up data. It is more like Hash Table. It is better in this case.  
More difference between Map and Object, see [Javascript: Map VS Object](https://maorutian.github.io/2020/04/30/Javascript-Map-VS-Object/).

#### Why we use index(i) as value, number(x) as key?

Because when we check whether the number exists in the map, we use `map.has()`. This method returns a boolean indicating whether an element with the specified KEY exists or not. So we use number as key. Once we find it, we can use `map.get()` to get the value in the map - index(i).

### Code

```
var twoSum = function (nums, target) {
      const map = new Map();
      for (let i = 0; i < nums.length; i++) {
        const x = target - nums[i];
        if (map.has(x)) {
          return [i, map.get(x)];
        } else {
          map.set(nums[i], i);
        }
      }
      return [];
    };
```

### Complexity Analysis

* Time complexity : `O(n)`. We traverse the list containing elements only once `O(n)`. Each look up in the table costs only `O(1)` time.

* Space complexity : `O(n)`. The extra space required depends on the number of items stored in the hash table, which stores at most nn elements.




