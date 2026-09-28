<h1 align="center">🧩 DSA Pattern Mastery</h1>
<p align="center"><b>Two Pointers &amp; Sliding Window · Prefix Sum · Merge Intervals</b><br>A phase-by-phase LeetCode roadmap that builds from fundamentals to hard capstone problems.</p>
<p align="center">
<img alt="Entries" src="https://img.shields.io/badge/entries-133-blue">
<img alt="Unique" src="https://img.shields.io/badge/unique%20problems-110-blueviolet">
<img alt="Easy" src="https://img.shields.io/badge/easy-23-brightgreen">
<img alt="Medium" src="https://img.shields.io/badge/medium-75-yellow">
<img alt="Hard" src="https://img.shields.io/badge/hard-35-red">
</p>

---

## 📖 How to use this roadmap

1. Go **top to bottom** inside a pattern. Each phase assumes the previous one.
2. Track progress by changing `- [ ]` to `- [x]` (clickable if you view this in a GitHub Issue, PR or Gist).
3. Use the **priority stars** to decide where to spend extra practice time.
4. Hit a wall? Re-read the pattern cheat sheet below, then retry before looking at solutions.
5. Do the **Capstone Review** phase only after every earlier phase in that pattern is done.

### Legend

| Symbol | Meaning |
|:---:|---|
| 🟢 🟡 🔴 | Easy / Medium / Hard |
| ⭐ | Nice to know. One solid pass is enough |
| ⭐⭐⭐ | Important. Solve it again after a week |
| ⭐⭐⭐⭐⭐ | Critical. Comes up constantly, so you should be able to write it cold |
| 🔁 | Repeat. The problem already appeared in an earlier phase, so it is intentional spaced repetition |

---

## 📊 At a glance

| Pattern | Phases | Entries | 🟢 Easy | 🟡 Medium | 🔴 Hard | Unique |
|---|:---:|:---:|:---:|:---:|:---:|:---:|
| [🔹 Two Pointers & Sliding Window](#two-pointers) | 9 | 55 | 12 | 31 | 12 | 49 |
| [🔸 Prefix Sum](#prefix-sum) | 11 | 49 | 8 | 29 | 12 | 40 |
| [🔷 Merge Intervals](#merge-intervals) | 8 | 29 | 3 | 15 | 11 | 26 |
| **Total** | | **133** | **23** | **75** | **35** | **110** |

> 💡 Some problems appear in more than one phase on purpose. That is why there are 133 entries but only 110 unique problems (23 easy, 62 medium, 25 hard).

---

## 🧠 Pattern cheat sheet

| Pattern | Reach for it when… | Core idea |
|---|---|---|
| Two pointers (opposite) | Sorted array, pair/triplet search, palindromes | Move the left or right pointer based on the current sum or comparison |
| Fast & slow pointers | Cycles, middle of a list, repeated values | Two speeds meet inside a cycle |
| Fixed sliding window | "Subarray or substring of size K" | Add the new element, drop the old one, update the answer |
| Variable sliding window | Longest or shortest subarray meeting a condition | Expand right, shrink left while the window is invalid |
| At most K | "Exactly K" counting | `exactly(K) = atMost(K) - atMost(K-1)` |
| Monotonic deque | Window min or max, sum constraints with negatives | Keep candidates in order, pop the ones that can never win |
| Prefix sum + hashmap | Count or find subarrays with a target sum | `sum(i..j) = P[j] - P[i-1]`, so look up `P[j] - target` |
| Prefix sum + modulo | Divisibility by K | Two prefixes with the same remainder bound a divisible subarray |
| 2D prefix sum | Rectangle sums, submatrix queries | Inclusion-exclusion on four corners |
| Difference array | Many range updates, one final read | `d[l] += v`, `d[r+1] -= v`, then prefix-sum it |
| Merge intervals | Overlaps, merging, inserting | Sort by start, then compare with the last merged interval |
| Greedy intervals | Max non-overlapping, min arrows or removals | Sort by end, keep whatever finishes earliest |
| Sweep line | Max concurrent events, skyline | Turn intervals into +1/-1 events, sort, scan |
| Interval + heap | Rooms, chairs, free time, queries | Heap of active end times, pop the ones that expired |

<details>
<summary><b>Templates worth memorising</b></summary>

```python
# Variable sliding window (longest valid)
left = best = 0
for right, x in enumerate(nums):
    add(x)
    while not valid():
        remove(nums[left]); left += 1
    best = max(best, right - left + 1)

# Prefix sum + hashmap (count subarrays with sum == k)
seen = {0: 1}; pre = ans = 0
for x in nums:
    pre += x
    ans += seen.get(pre - k, 0)
    seen[pre] = seen.get(pre, 0) + 1

# Merge intervals
intervals.sort()
merged = []
for s, e in intervals:
    if merged and s <= merged[-1][1]:
        merged[-1][1] = max(merged[-1][1], e)
    else:
        merged.append([s, e])
```

</details>

---

## 🚀 Suggested path

| Week | Focus |
|:---:|---|
| 1 | Two Pointers phases 1 to 3 |
| 2 | Sliding Window phases 4 to 7 |
| 3 | Monotonic Deque, Two Pointers capstone, Prefix Sum phases 1 to 4 |
| 4 | Prefix Sum phases 5 to 11 |
| 5 | Merge Intervals phases 1 to 5 |
| 6 | Merge Intervals phases 6 to 8, then re-do every ⭐⭐⭐⭐⭐ |

> Adjust the pace to your schedule. What matters is finishing a phase before starting the next.

---

## 🎯 Must-do problems (⭐⭐⭐⭐⭐)

- 🔴 <a href="https://leetcode.com/problems/substring-with-concatenation-of-all-words/" target="_blank" rel="noopener noreferrer">30. Substring with Concatenation of All Words</a>
- 🔴 <a href="https://leetcode.com/problems/minimum-window-substring/" target="_blank" rel="noopener noreferrer">76. Minimum Window Substring</a>
- 🔴 <a href="https://leetcode.com/problems/sliding-window-maximum/" target="_blank" rel="noopener noreferrer">239. Sliding Window Maximum</a>
- 🔴 <a href="https://leetcode.com/problems/range-module/" target="_blank" rel="noopener noreferrer">715. Range Module</a>
- 🔴 <a href="https://leetcode.com/problems/my-calendar-iii/" target="_blank" rel="noopener noreferrer">732. My Calendar III</a>
- 🔴 <a href="https://leetcode.com/problems/shortest-subarray-with-sum-at-least-k/" target="_blank" rel="noopener noreferrer">862. Shortest Subarray with Sum at Least K</a>
- 🔴 <a href="https://leetcode.com/problems/subarrays-with-k-different-integers/" target="_blank" rel="noopener noreferrer">992. Subarrays with K Different Integers</a>
- 🟡 <a href="https://leetcode.com/problems/longest-continuous-subarray-with-absolute-diff-less-than-or-equal-to-limit/" target="_blank" rel="noopener noreferrer">1438. Longest Continuous Subarray With Absolute Diff Less Than or Equal to Limit</a>
- 🔴 <a href="https://leetcode.com/problems/minimum-interval-to-include-each-query/" target="_blank" rel="noopener noreferrer">1851. Minimum Interval to Include Each Query</a>
- 🔴 <a href="https://leetcode.com/problems/meeting-rooms-iii/" target="_blank" rel="noopener noreferrer">2402. Meeting Rooms III</a>

---

<a id="two-pointers"></a>

## 🔹 Two Pointers & Sliding Window

`55 problems` · 🟢 12 Easy · 🟡 31 Medium · 🔴 12 Hard

<details>
<summary><b>Phase 1 · Fundamentals</b> &nbsp;<sub>(8 problems)</sub></summary>

- [ ] 🟢 <a href="https://leetcode.com/problems/reverse-string/" target="_blank" rel="noopener noreferrer">344. Reverse String</a>
- [ ] 🟢 <a href="https://leetcode.com/problems/valid-palindrome/" target="_blank" rel="noopener noreferrer">125. Valid Palindrome</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/" target="_blank" rel="noopener noreferrer">167. Two Sum II - Input Array Is Sorted</a>
- [ ] 🟢 <a href="https://leetcode.com/problems/move-zeroes/" target="_blank" rel="noopener noreferrer">283. Move Zeroes</a>
- [ ] 🟢 <a href="https://leetcode.com/problems/remove-duplicates-from-sorted-array/" target="_blank" rel="noopener noreferrer">26. Remove Duplicates from Sorted Array</a>
- [ ] 🟢 <a href="https://leetcode.com/problems/remove-element/" target="_blank" rel="noopener noreferrer">27. Remove Element</a>
- [ ] 🟢 <a href="https://leetcode.com/problems/squares-of-a-sorted-array/" target="_blank" rel="noopener noreferrer">977. Squares of a Sorted Array</a>
- [ ] 🟢 <a href="https://leetcode.com/problems/merge-sorted-array/" target="_blank" rel="noopener noreferrer">88. Merge Sorted Array</a>

</details>

<details>
<summary><b>Phase 2 · Opposite Pointers</b> &nbsp;<sub>(7 problems)</sub></summary>

- [ ] 🟡 <a href="https://leetcode.com/problems/container-with-most-water/" target="_blank" rel="noopener noreferrer">11. Container With Most Water</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/3sum/" target="_blank" rel="noopener noreferrer">15. 3Sum</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/3sum-closest/" target="_blank" rel="noopener noreferrer">16. 3Sum Closest</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/4sum/" target="_blank" rel="noopener noreferrer">18. 4Sum</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/3sum-smaller/" target="_blank" rel="noopener noreferrer">259. 3Sum Smaller</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/valid-triangle-number/" target="_blank" rel="noopener noreferrer">611. Valid Triangle Number</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/boats-to-save-people/" target="_blank" rel="noopener noreferrer">881. Boats to Save People</a>

</details>

<details>
<summary><b>Phase 3 · Fast & Slow Pointers</b> &nbsp;<sub>(6 problems)</sub></summary>

- [ ] 🟢 <a href="https://leetcode.com/problems/linked-list-cycle/" target="_blank" rel="noopener noreferrer">141. Linked List Cycle</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/linked-list-cycle-ii/" target="_blank" rel="noopener noreferrer">142. Linked List Cycle II</a>
- [ ] 🟢 <a href="https://leetcode.com/problems/middle-of-the-linked-list/" target="_blank" rel="noopener noreferrer">876. Middle of the Linked List</a>
- [ ] 🟢 <a href="https://leetcode.com/problems/happy-number/" target="_blank" rel="noopener noreferrer">202. Happy Number</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/find-the-duplicate-number/" target="_blank" rel="noopener noreferrer">287. Find the Duplicate Number</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/circular-array-loop/" target="_blank" rel="noopener noreferrer">457. Circular Array Loop</a>

</details>

<details>
<summary><b>Phase 4 · Fixed Sliding Window</b> &nbsp;<sub>(6 problems)</sub></summary>

- [ ] 🟢 <a href="https://leetcode.com/problems/maximum-average-subarray-i/" target="_blank" rel="noopener noreferrer">643. Maximum Average Subarray I</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/number-of-sub-arrays-of-size-k-and-average-greater-than-or-equal-to-threshold/" target="_blank" rel="noopener noreferrer">1343. Number of Sub-arrays of Size K and Average Greater than or Equal to Threshold</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/maximum-number-of-vowels-in-a-substring-of-given-length/" target="_blank" rel="noopener noreferrer">1456. Maximum Number of Vowels in a Substring of Given Length</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/grumpy-bookstore-owner/" target="_blank" rel="noopener noreferrer">1052. Grumpy Bookstore Owner</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/permutation-in-string/" target="_blank" rel="noopener noreferrer">567. Permutation in String</a> ⭐
- [ ] 🟡 <a href="https://leetcode.com/problems/find-all-anagrams-in-a-string/" target="_blank" rel="noopener noreferrer">438. Find All Anagrams in a String</a> ⭐

</details>

<details>
<summary><b>Phase 5 · Variable Sliding Window</b> &nbsp;<sub>(8 problems)</sub></summary>

- [ ] 🟢 <a href="https://leetcode.com/problems/find-the-index-of-the-first-occurrence-in-a-string/" target="_blank" rel="noopener noreferrer">28. Find the Index of the First Occurrence in a String</a> ⭐⭐⭐
- [ ] 🟡 <a href="https://leetcode.com/problems/minimum-size-subarray-sum/" target="_blank" rel="noopener noreferrer">209. Minimum Size Subarray Sum</a> ⭐
- [ ] 🟡 <a href="https://leetcode.com/problems/max-consecutive-ones-iii/" target="_blank" rel="noopener noreferrer">1004. Max Consecutive Ones III</a> ⭐
- [ ] 🟡 <a href="https://leetcode.com/problems/longest-subarray-of-1s-after-deleting-one-element/" target="_blank" rel="noopener noreferrer">1493. Longest Subarray of 1's After Deleting One Element</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/subarray-product-less-than-k/" target="_blank" rel="noopener noreferrer">713. Subarray Product Less Than K</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/fruit-into-baskets/" target="_blank" rel="noopener noreferrer">904. Fruit Into Baskets</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/maximum-erasure-value/" target="_blank" rel="noopener noreferrer">1695. Maximum Erasure Value</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/get-equal-substrings-within-budget/" target="_blank" rel="noopener noreferrer">1208. Get Equal Substrings Within Budget</a>

</details>

<details>
<summary><b>Phase 6 · Frequency Window</b> &nbsp;<sub>(5 problems)</sub></summary>

- [ ] 🔴 <a href="https://leetcode.com/problems/minimum-window-substring/" target="_blank" rel="noopener noreferrer">76. Minimum Window Substring</a> ⭐⭐⭐⭐⭐
- [ ] 🟡 <a href="https://leetcode.com/problems/longest-repeating-character-replacement/" target="_blank" rel="noopener noreferrer">424. Longest Repeating Character Replacement</a> ⭐⭐⭐⭐
- [ ] 🔴 <a href="https://leetcode.com/problems/substring-with-concatenation-of-all-words/" target="_blank" rel="noopener noreferrer">30. Substring with Concatenation of All Words</a> ⭐⭐⭐⭐⭐
- [ ] 🟡 <a href="https://leetcode.com/problems/number-of-substrings-containing-all-three-characters/" target="_blank" rel="noopener noreferrer">1358. Number of Substrings Containing All Three Characters</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/find-all-anagrams-in-a-string/" target="_blank" rel="noopener noreferrer">438. Find All Anagrams in a String</a> 🔁 ⭐

</details>

<details>
<summary><b>Phase 7 · At Most K</b> &nbsp;<sub>(4 problems)</sub></summary>

- [ ] 🔴 <a href="https://leetcode.com/problems/subarrays-with-k-different-integers/" target="_blank" rel="noopener noreferrer">992. Subarrays with K Different Integers</a> ⭐⭐⭐⭐⭐
- [ ] 🟡 <a href="https://leetcode.com/problems/binary-subarrays-with-sum/" target="_blank" rel="noopener noreferrer">930. Binary Subarrays With Sum</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/count-number-of-nice-subarrays/" target="_blank" rel="noopener noreferrer">1248. Count Number of Nice Subarrays</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/number-of-substrings-containing-all-three-characters/" target="_blank" rel="noopener noreferrer">1358. Number of Substrings Containing All Three Characters</a> 🔁

</details>

<details>
<summary><b>Phase 8 · Monotonic Deque</b> &nbsp;<sub>(5 problems)</sub></summary>

- [ ] 🔴 <a href="https://leetcode.com/problems/sliding-window-maximum/" target="_blank" rel="noopener noreferrer">239. Sliding Window Maximum</a> ⭐⭐⭐⭐⭐
- [ ] 🟡 <a href="https://leetcode.com/problems/longest-continuous-subarray-with-absolute-diff-less-than-or-equal-to-limit/" target="_blank" rel="noopener noreferrer">1438. Longest Continuous Subarray With Absolute Diff Less Than or Equal to Limit</a> ⭐⭐⭐⭐⭐
- [ ] 🔴 <a href="https://leetcode.com/problems/shortest-subarray-with-sum-at-least-k/" target="_blank" rel="noopener noreferrer">862. Shortest Subarray with Sum at Least K</a> ⭐⭐⭐⭐⭐
- [ ] 🔴 <a href="https://leetcode.com/problems/max-value-of-equation/" target="_blank" rel="noopener noreferrer">1499. Max Value of Equation</a>
- [ ] 🔴 <a href="https://leetcode.com/problems/constrained-subsequence-sum/" target="_blank" rel="noopener noreferrer">1425. Constrained Subsequence Sum</a>

</details>

<details>
<summary><b>Phase 9 · Capstone Review</b> &nbsp;<sub>(6 problems)</sub></summary>

- [ ] 🔴 <a href="https://leetcode.com/problems/trapping-rain-water/" target="_blank" rel="noopener noreferrer">42. Trapping Rain Water</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/number-of-subsequences-that-satisfy-the-given-sum-condition/" target="_blank" rel="noopener noreferrer">1498. Number of Subsequences That Satisfy the Given Sum Condition</a>
- [ ] 🔴 <a href="https://leetcode.com/problems/substring-with-concatenation-of-all-words/" target="_blank" rel="noopener noreferrer">30. Substring with Concatenation of All Words</a> 🔁 ⭐⭐⭐⭐⭐
- [ ] 🔴 <a href="https://leetcode.com/problems/minimum-window-substring/" target="_blank" rel="noopener noreferrer">76. Minimum Window Substring</a> 🔁 ⭐⭐⭐⭐⭐
- [ ] 🔴 <a href="https://leetcode.com/problems/subarrays-with-k-different-integers/" target="_blank" rel="noopener noreferrer">992. Subarrays with K Different Integers</a> 🔁 ⭐⭐⭐⭐⭐
- [ ] 🔴 <a href="https://leetcode.com/problems/sliding-window-maximum/" target="_blank" rel="noopener noreferrer">239. Sliding Window Maximum</a> 🔁 ⭐⭐⭐⭐⭐

</details>

<a id="prefix-sum"></a>

## 🔸 Prefix Sum

`49 problems` · 🟢 8 Easy · 🟡 29 Medium · 🔴 12 Hard

<details>
<summary><b>Phase 1 · Foundation</b> &nbsp;<sub>(7 problems)</sub></summary>

- [ ] 🟢 <a href="https://leetcode.com/problems/running-sum-of-1d-array/" target="_blank" rel="noopener noreferrer">1480. Running Sum of 1d Array</a>
- [ ] 🟢 <a href="https://leetcode.com/problems/range-sum-query-immutable/" target="_blank" rel="noopener noreferrer">303. Range Sum Query - Immutable</a>
- [ ] 🟢 <a href="https://leetcode.com/problems/find-pivot-index/" target="_blank" rel="noopener noreferrer">724. Find Pivot Index</a>
- [ ] 🟢 <a href="https://leetcode.com/problems/find-the-middle-index-in-array/" target="_blank" rel="noopener noreferrer">1991. Find the Middle Index in Array</a>
- [ ] 🟢 <a href="https://leetcode.com/problems/left-and-right-sum-differences/" target="_blank" rel="noopener noreferrer">2574. Left and Right Sum Differences</a>
- [ ] 🟢 <a href="https://leetcode.com/problems/sum-of-all-odd-length-subarrays/" target="_blank" rel="noopener noreferrer">1588. Sum of All Odd Length Subarrays</a>
- [ ] 🟢 <a href="https://leetcode.com/problems/find-the-highest-altitude/" target="_blank" rel="noopener noreferrer">1732. Find the Highest Altitude</a>

</details>

<details>
<summary><b>Phase 2 · + Hashmap</b> &nbsp;<sub>(6 problems)</sub></summary>

- [ ] 🟡 <a href="https://leetcode.com/problems/subarray-sum-equals-k/" target="_blank" rel="noopener noreferrer">560. Subarray Sum Equals K</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/subarray-sums-divisible-by-k/" target="_blank" rel="noopener noreferrer">974. Subarray Sums Divisible by K</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/contiguous-array/" target="_blank" rel="noopener noreferrer">525. Contiguous Array</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/binary-subarrays-with-sum/" target="_blank" rel="noopener noreferrer">930. Binary Subarrays With Sum</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/count-number-of-nice-subarrays/" target="_blank" rel="noopener noreferrer">1248. Count Number of Nice Subarrays</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/make-sum-divisible-by-p/" target="_blank" rel="noopener noreferrer">1590. Make Sum Divisible by P</a>

</details>

<details>
<summary><b>Phase 3 · + Modulo</b> &nbsp;<sub>(5 problems)</sub></summary>

- [ ] 🟡 <a href="https://leetcode.com/problems/continuous-subarray-sum/" target="_blank" rel="noopener noreferrer">523. Continuous Subarray Sum</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/subarray-sums-divisible-by-k/" target="_blank" rel="noopener noreferrer">974. Subarray Sums Divisible by K</a> 🔁
- [ ] 🟡 <a href="https://leetcode.com/problems/make-sum-divisible-by-p/" target="_blank" rel="noopener noreferrer">1590. Make Sum Divisible by P</a> 🔁
- [ ] 🟡 <a href="https://leetcode.com/problems/count-of-interesting-subarrays/" target="_blank" rel="noopener noreferrer">2845. Count of Interesting Subarrays</a>
- [ ] 🔴 <a href="https://leetcode.com/problems/count-subarrays-with-median-k/" target="_blank" rel="noopener noreferrer">2488. Count Subarrays With Median K</a>

</details>

<details>
<summary><b>Phase 4 · + Transformation</b> &nbsp;<sub>(5 problems)</sub></summary>

- [ ] 🟡 <a href="https://leetcode.com/problems/contiguous-array/" target="_blank" rel="noopener noreferrer">525. Contiguous Array</a> 🔁
- [ ] 🟡 <a href="https://leetcode.com/problems/longest-well-performing-interval/" target="_blank" rel="noopener noreferrer">1124. Longest Well-Performing Interval</a>
- [ ] 🔴 <a href="https://leetcode.com/problems/count-subarrays-with-median-k/" target="_blank" rel="noopener noreferrer">2488. Count Subarrays With Median K</a> 🔁
- [ ] 🟡 <a href="https://leetcode.com/problems/maximum-number-of-non-overlapping-subarrays-with-sum-equals-target/" target="_blank" rel="noopener noreferrer">1546. Maximum Number of Non-Overlapping Subarrays With Sum Equals Target</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/count-triplets-that-can-form-two-arrays-of-equal-xor/" target="_blank" rel="noopener noreferrer">1442. Count Triplets That Can Form Two Arrays of Equal XOR</a>

</details>

<details>
<summary><b>Phase 5 · 2D Prefix Sum</b> &nbsp;<sub>(5 problems)</sub></summary>

- [ ] 🟡 <a href="https://leetcode.com/problems/matrix-block-sum/" target="_blank" rel="noopener noreferrer">1314. Matrix Block Sum</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/range-sum-query-2d-immutable/" target="_blank" rel="noopener noreferrer">304. Range Sum Query 2D - Immutable</a>
- [ ] 🔴 <a href="https://leetcode.com/problems/number-of-submatrices-that-sum-to-target/" target="_blank" rel="noopener noreferrer">1074. Number of Submatrices That Sum to Target</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/maximum-side-length-of-a-square-with-sum-less-than-or-equal-to-threshold/" target="_blank" rel="noopener noreferrer">1292. Maximum Side Length of a Square with Sum Less than or Equal to Threshold</a>
- [ ] 🔴 <a href="https://leetcode.com/problems/max-sum-of-rectangle-no-larger-than-k/" target="_blank" rel="noopener noreferrer">363. Max Sum of Rectangle No Larger Than K</a>

</details>

<details>
<summary><b>Phase 6 · + Binary Search</b> &nbsp;<sub>(5 problems)</sub></summary>

- [ ] 🟡 <a href="https://leetcode.com/problems/minimum-size-subarray-sum/" target="_blank" rel="noopener noreferrer">209. Minimum Size Subarray Sum</a> ⭐
- [ ] 🔴 <a href="https://leetcode.com/problems/shortest-subarray-with-sum-at-least-k/" target="_blank" rel="noopener noreferrer">862. Shortest Subarray with Sum at Least K</a> ⭐⭐⭐⭐⭐
- [ ] 🟢 <a href="https://leetcode.com/problems/longest-subsequence-with-limited-sum/" target="_blank" rel="noopener noreferrer">2389. Longest Subsequence With Limited Sum</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/compare-strings-by-frequency-of-the-smallest-character/" target="_blank" rel="noopener noreferrer">1170. Compare Strings by Frequency of the Smallest Character</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/random-pick-with-weight/" target="_blank" rel="noopener noreferrer">528. Random Pick with Weight</a>

</details>

<details>
<summary><b>Phase 7 · + Monotonic Deque</b> &nbsp;<sub>(1 problem)</sub></summary>

- [ ] 🔴 <a href="https://leetcode.com/problems/shortest-subarray-with-sum-at-least-k/" target="_blank" rel="noopener noreferrer">862. Shortest Subarray with Sum at Least K</a> 🔁 ⭐⭐⭐⭐⭐

</details>

<details>
<summary><b>Phase 8 · + OrderedSet / Tree</b> &nbsp;<sub>(1 problem)</sub></summary>

- [ ] 🔴 <a href="https://leetcode.com/problems/max-sum-of-rectangle-no-larger-than-k/" target="_blank" rel="noopener noreferrer">363. Max Sum of Rectangle No Larger Than K</a> 🔁

</details>

<details>
<summary><b>Phase 9 · + Hashmap + 2D</b> &nbsp;<sub>(1 problem)</sub></summary>

- [ ] 🔴 <a href="https://leetcode.com/problems/number-of-submatrices-that-sum-to-target/" target="_blank" rel="noopener noreferrer">1074. Number of Submatrices That Sum to Target</a> 🔁

</details>

<details>
<summary><b>Phase 10 · + Difference Array</b> &nbsp;<sub>(3 problems)</sub></summary>

- [ ] 🟡 <a href="https://leetcode.com/problems/corporate-flight-bookings/" target="_blank" rel="noopener noreferrer">1109. Corporate Flight Bookings</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/car-pooling/" target="_blank" rel="noopener noreferrer">1094. Car Pooling</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/increment-submatrices-by-one/" target="_blank" rel="noopener noreferrer">2536. Increment Submatrices by One</a>

</details>

<details>
<summary><b>Phase 11 · Capstone Review</b> &nbsp;<sub>(10 problems)</sub></summary>

- [ ] 🔴 <a href="https://leetcode.com/problems/count-of-range-sum/" target="_blank" rel="noopener noreferrer">327. Count of Range Sum</a>
- [ ] 🔴 <a href="https://leetcode.com/problems/reverse-pairs/" target="_blank" rel="noopener noreferrer">493. Reverse Pairs</a>
- [ ] 🔴 <a href="https://leetcode.com/problems/count-of-smaller-numbers-after-self/" target="_blank" rel="noopener noreferrer">315. Count of Smaller Numbers After Self</a>
- [ ] 🔴 <a href="https://leetcode.com/problems/find-longest-awesome-substring/" target="_blank" rel="noopener noreferrer">1542. Find Longest Awesome Substring</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/number-of-wonderful-substrings/" target="_blank" rel="noopener noreferrer">1915. Number of Wonderful Substrings</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/number-of-sub-arrays-with-odd-sum/" target="_blank" rel="noopener noreferrer">1524. Number of Sub-arrays With Odd Sum</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/count-triplets-that-can-form-two-arrays-of-equal-xor/" target="_blank" rel="noopener noreferrer">1442. Count Triplets That Can Form Two Arrays of Equal XOR</a> 🔁
- [ ] 🟡 <a href="https://leetcode.com/problems/remove-zero-sum-consecutive-nodes-from-linked-list/" target="_blank" rel="noopener noreferrer">1171. Remove Zero Sum Consecutive Nodes from Linked List</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/minimum-penalty-for-a-shop/" target="_blank" rel="noopener noreferrer">2483. Minimum Penalty for a Shop</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/longest-well-performing-interval/" target="_blank" rel="noopener noreferrer">1124. Longest Well-Performing Interval</a> 🔁

</details>

<a id="merge-intervals"></a>

## 🔷 Merge Intervals

`29 problems` · 🟢 3 Easy · 🟡 15 Medium · 🔴 11 Hard

<details>
<summary><b>Phase 1 · Fundamentals</b> &nbsp;<sub>(4 problems)</sub></summary>

- [ ] 🟢 <a href="https://leetcode.com/problems/summary-ranges/" target="_blank" rel="noopener noreferrer">228. Summary Ranges</a>
- [ ] 🟢 <a href="https://leetcode.com/problems/missing-ranges/" target="_blank" rel="noopener noreferrer">163. Missing Ranges</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/merge-intervals/" target="_blank" rel="noopener noreferrer">56. Merge Intervals</a> ⭐
- [ ] 🟡 <a href="https://leetcode.com/problems/insert-interval/" target="_blank" rel="noopener noreferrer">57. Insert Interval</a> ⭐

</details>

<details>
<summary><b>Phase 2 · Overlap & Greedy</b> &nbsp;<sub>(5 problems)</sub></summary>

- [ ] 🟢 <a href="https://leetcode.com/problems/meeting-rooms/" target="_blank" rel="noopener noreferrer">252. Meeting Rooms</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/meeting-rooms-ii/" target="_blank" rel="noopener noreferrer">253. Meeting Rooms II</a> ⭐⭐⭐⭐
- [ ] 🟡 <a href="https://leetcode.com/problems/non-overlapping-intervals/" target="_blank" rel="noopener noreferrer">435. Non-overlapping Intervals</a> ⭐⭐⭐
- [ ] 🟡 <a href="https://leetcode.com/problems/minimum-number-of-arrows-to-burst-balloons/" target="_blank" rel="noopener noreferrer">452. Minimum Number of Arrows to Burst Balloons</a> ⭐⭐⭐
- [ ] 🟡 <a href="https://leetcode.com/problems/remove-covered-intervals/" target="_blank" rel="noopener noreferrer">1288. Remove Covered Intervals</a>

</details>

<details>
<summary><b>Phase 3 · Interval Relationships</b> &nbsp;<sub>(3 problems)</sub></summary>

- [ ] 🟡 <a href="https://leetcode.com/problems/interval-list-intersections/" target="_blank" rel="noopener noreferrer">986. Interval List Intersections</a> ⭐⭐⭐
- [ ] 🟡 <a href="https://leetcode.com/problems/partition-labels/" target="_blank" rel="noopener noreferrer">763. Partition Labels</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/remove-interval/" target="_blank" rel="noopener noreferrer">1272. Remove Interval</a>

</details>

<details>
<summary><b>Phase 4 · Scheduling</b> &nbsp;<sub>(3 problems)</sub></summary>

- [ ] 🟡 <a href="https://leetcode.com/problems/the-number-of-the-smallest-unoccupied-chair/" target="_blank" rel="noopener noreferrer">1942. The Number of the Smallest Unoccupied Chair</a> ⭐⭐⭐⭐
- [ ] 🔴 <a href="https://leetcode.com/problems/meeting-rooms-iii/" target="_blank" rel="noopener noreferrer">2402. Meeting Rooms III</a> ⭐⭐⭐⭐⭐
- [ ] 🔴 <a href="https://leetcode.com/problems/employee-free-time/" target="_blank" rel="noopener noreferrer">759. Employee Free Time</a> ⭐⭐⭐⭐

</details>

<details>
<summary><b>Phase 5 · Sweep Line</b> &nbsp;<sub>(3 problems)</sub></summary>

- [ ] 🟡 <a href="https://leetcode.com/problems/car-pooling/" target="_blank" rel="noopener noreferrer">1094. Car Pooling</a>
- [ ] 🟡 <a href="https://leetcode.com/problems/my-calendar-ii/" target="_blank" rel="noopener noreferrer">731. My Calendar II</a> ⭐⭐⭐⭐
- [ ] 🔴 <a href="https://leetcode.com/problems/my-calendar-iii/" target="_blank" rel="noopener noreferrer">732. My Calendar III</a> ⭐⭐⭐⭐⭐

</details>

<details>
<summary><b>Phase 6 · Interval + Heap</b> &nbsp;<sub>(3 problems)</sub></summary>

- [ ] 🟡 <a href="https://leetcode.com/problems/meeting-rooms-ii/" target="_blank" rel="noopener noreferrer">253. Meeting Rooms II</a> 🔁 ⭐⭐⭐⭐
- [ ] 🔴 <a href="https://leetcode.com/problems/minimum-interval-to-include-each-query/" target="_blank" rel="noopener noreferrer">1851. Minimum Interval to Include Each Query</a> ⭐⭐⭐⭐⭐
- [ ] 🔴 <a href="https://leetcode.com/problems/employee-free-time/" target="_blank" rel="noopener noreferrer">759. Employee Free Time</a> 🔁 ⭐⭐⭐⭐

</details>

<details>
<summary><b>Phase 7 · Interval Coverage</b> &nbsp;<sub>(4 problems)</sub></summary>

- [ ] 🟡 <a href="https://leetcode.com/problems/video-stitching/" target="_blank" rel="noopener noreferrer">1024. Video Stitching</a> ⭐⭐⭐⭐
- [ ] 🔴 <a href="https://leetcode.com/problems/minimum-number-of-taps-to-open-to-water-a-garden/" target="_blank" rel="noopener noreferrer">1326. Minimum Number of Taps to Open to Water a Garden</a> ⭐⭐⭐⭐
- [ ] 🟡 <a href="https://leetcode.com/problems/remove-interval/" target="_blank" rel="noopener noreferrer">1272. Remove Interval</a> 🔁
- [ ] 🔴 <a href="https://leetcode.com/problems/range-module/" target="_blank" rel="noopener noreferrer">715. Range Module</a> ⭐⭐⭐⭐⭐

</details>

<details>
<summary><b>Phase 8 · Capstone Review</b> &nbsp;<sub>(4 problems)</sub></summary>

- [ ] 🔴 <a href="https://leetcode.com/problems/the-skyline-problem/" target="_blank" rel="noopener noreferrer">218. The Skyline Problem</a>
- [ ] 🔴 <a href="https://leetcode.com/problems/perfect-rectangle/" target="_blank" rel="noopener noreferrer">391. Perfect Rectangle</a>
- [ ] 🔴 <a href="https://leetcode.com/problems/rectangle-area-ii/" target="_blank" rel="noopener noreferrer">850. Rectangle Area II</a>
- [ ] 🔴 <a href="https://leetcode.com/problems/falling-squares/" target="_blank" rel="noopener noreferrer">699. Falling Squares</a>

</details>

---

<p align="center"><i>133 entries · 110 unique problems · 3 patterns · built for structured, repeatable DSA practice 🚀</i></p>
