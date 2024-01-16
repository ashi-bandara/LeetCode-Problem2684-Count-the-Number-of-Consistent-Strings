
# LeetCode Challenge D32
## Achievements
[![image.png](https://i.postimg.cc/P57GM7nZ/image.png)](https://postimg.cc/YvQyrb9q)
This solution outperformed 83.41% of Java users on LeetCode according to runtime metrics and 63.29% according to Memory metrics.


## Overview

Welcome to my LeetCode solution repository! This project addresses the coding challenge presented by [[1684. Count the Number of Consistent Strings](https://leetcode.com/problems/count-the-number-of-consistent-strings/). Below, you'll find details about the problem, my approach to solving it, and the implemented solution.

## Problem Statement
Given a string  `allowed`  consisting of  **distinct**  characters and an array of strings  `words`, a string is  **consistent** if all characters in the string appear in the string  `allowed`.
Return _the number of  **consistent**  strings in the array_ `words`.

**Example**

> **Input:** allowed = "ab", words = ["ad","bd","aaab","baa","badab"]
> 
>**Output:** 2
> 
>**Explanation:** 
>Strings "aaab" and "baa" are consistent since they only contain characters 'a' and 'b'.

**Language Used**
> Java

**Difficulty**
> Easy

## Solution Overview

The provided Java solution aims to count the number of consistent strings within an array based on a specified set of allowed characters. The algorithm employs a HashSet, named `allowedArray`, to store unique characters extracted from the input string, `allowed`. This HashSet serves as an efficient data structure for subsequent character comparison.

The initialization phase involves setting up a counter variable, `count`, to track the number of consistent strings, and creating the HashSet to facilitate quick character lookups. The algorithm then populates `allowedArray` by iterating over each character in the `allowed` string. Subsequently, the code iterates through each word in the `words` array. For each word, a boolean variable, `isConsistent`, is initialized to `true`. The algorithm then scrutinizes each character within the word, employing a nested loop for character-level analysis.

During the character comparison process, the code checks whether each character in the word is present in the previously constructed `allowedArray` HashSet. If a character is not found, the `isConsistent` variable is set to `false`, signifying that the word is not consistent. The loop breaks to avoid unnecessary further checks, as the presence of a single non-matching character renders the word inconsistent. Upon completing the character-level analysis, the algorithm checks the final state of `isConsistent`. If it remains `true`, indicating that the entire word is consistent, the `count` variable is incremented.
