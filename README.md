# 🧩 DSA Pattern Mastery

**Two Pointers & Sliding Window · Prefix Sum · Merge Intervals**

A phase-by-phase LeetCode roadmap — each phase builds on the last, from fundamentals to hardest capstone problems.

![Total](https://img.shields.io/badge/total-133%20problems-blue)
![Easy](https://img.shields.io/badge/easy-23-brightgreen)
![Medium](https://img.shields.io/badge/medium-75-yellow)
![Hard](https://img.shields.io/badge/hard-35-red)

### How to track progress
Check a box by editing the file and turning `- [ ]` into `- [x]` (or click it if you're viewing this via a GitHub Issue/PR/Gist, where checkboxes are clickable). `⭐` marks problems worth extra practice rounds — the more stars, the higher priority.

### At a glance

| Pattern | Phases | Problems | Easy | Medium | Hard |
|---|:---:|:---:|:---:|:---:|:---:|
| [🔹 Two Pointers & Sliding Window](#two-pointers) | 9 | 55 | 🟢 12 | 🟡 31 | 🔴 12 |
| [🔸 Prefix Sum](#prefix-sum) | 11 | 49 | 🟢 8 | 🟡 29 | 🔴 12 |
| [🔷 Merge Intervals](#merge-intervals) | 8 | 29 | 🟢 3 | 🟡 15 | 🔴 11 |
| **Total** | | **133** | **23** | **75** | **35** |

### Jump to a pattern
- [🔹 Two Pointers & Sliding Window](#two-pointers)
- [🔸 Prefix Sum](#prefix-sum)
- [🔷 Merge Intervals](#merge-intervals)

> 💡 Problems repeated in a **Capstone Review** phase are intentional spaced-repetition — tackle them once every earlier phase in that pattern is cleared.

---

## 🔹 Two Pointers & Sliding Window

`55 problems` · 🟢 12 Easy · 🟡 31 Medium · 🔴 12 Hard

<details>
<summary><b>Phase 1 · Fundamentals</b> &nbsp;<sub>(8 problems)</sub></summary>

- [ ] 🟢 [344. Reverse String](https://leetcode.com/problems/reverse-string/)
- [ ] 🟢 [125. Valid Palindrome](https://leetcode.com/problems/valid-palindrome/)
- [ ] 🟡 [167. Two Sum II - Input Array Is Sorted](https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/)
- [ ] 🟢 [283. Move Zeroes](https://leetcode.com/problems/move-zeroes/)
- [ ] 🟢 [26. Remove Duplicates from Sorted Array](https://leetcode.com/problems/remove-duplicates-from-sorted-array/)
- [ ] 🟢 [27. Remove Element](https://leetcode.com/problems/remove-element/)
- [ ] 🟢 [977. Squares of a Sorted Array](https://leetcode.com/problems/squares-of-a-sorted-array/)
- [ ] 🟢 [88. Merge Sorted Array](https://leetcode.com/problems/merge-sorted-array/)

</details>

<details>
<summary><b>Phase 2 · Opposite Pointers</b> &nbsp;<sub>(7 problems)</sub></summary>

- [ ] 🟡 [11. Container With Most Water](https://leetcode.com/problems/container-with-most-water/)
- [ ] 🟡 [15. 3Sum](https://leetcode.com/problems/3sum/)
- [ ] 🟡 [16. 3Sum Closest](https://leetcode.com/problems/3sum-closest/)
- [ ] 🟡 [18. 4Sum](https://leetcode.com/problems/4sum/)
- [ ] 🟡 [259. 3Sum Smaller](https://leetcode.com/problems/3sum-smaller/)
- [ ] 🟡 [611. Valid Triangle Number](https://leetcode.com/problems/valid-triangle-number/)
- [ ] 🟡 [881. Boats to Save People](https://leetcode.com/problems/boats-to-save-people/)

</details>

<details>
<summary><b>Phase 3 · Fast & Slow Pointers</b> &nbsp;<sub>(6 problems)</sub></summary>

- [ ] 🟢 [141. Linked List Cycle](https://leetcode.com/problems/linked-list-cycle/)
- [ ] 🟡 [142. Linked List Cycle II](https://leetcode.com/problems/linked-list-cycle-ii/)
- [ ] 🟢 [876. Middle of the Linked List](https://leetcode.com/problems/middle-of-the-linked-list/)
- [ ] 🟢 [202. Happy Number](https://leetcode.com/problems/happy-number/)
- [ ] 🟡 [287. Find the Duplicate Number](https://leetcode.com/problems/find-the-duplicate-number/)
- [ ] 🟡 [457. Circular Array Loop](https://leetcode.com/problems/circular-array-loop/)

</details>

<details>
<summary><b>Phase 4 · Fixed Sliding Window</b> &nbsp;<sub>(6 problems)</sub></summary>

- [ ] 🟢 [643. Maximum Average Subarray I](https://leetcode.com/problems/maximum-average-subarray-i/)
- [ ] 🟡 [1343. Number of Sub-arrays of Size K and Average Greater than or Equal to Threshold](https://leetcode.com/problems/number-of-sub-arrays-of-size-k-and-average-greater-than-or-equal-to-threshold/)
- [ ] 🟡 [1456. Maximum Number of Vowels in a Substring of Given Length](https://leetcode.com/problems/maximum-number-of-vowels-in-a-substring-of-given-length/)
- [ ] 🟡 [1052. Grumpy Bookstore Owner](https://leetcode.com/problems/grumpy-bookstore-owner/)
- [ ] 🟡 [567. Permutation in String](https://leetcode.com/problems/permutation-in-string/) `⭐`
- [ ] 🟡 [438. Find All Anagrams in a String](https://leetcode.com/problems/find-all-anagrams-in-a-string/) `⭐`

</details>

<details>
<summary><b>Phase 5 · Variable Sliding Window</b> &nbsp;<sub>(8 problems)</sub></summary>

- [ ] 🟢 [28. Find the Index of the First Occurrence in a String](https://leetcode.com/problems/find-the-index-of-the-first-occurrence-in-a-string/) `⭐⭐⭐`
- [ ] 🟡 [209. Minimum Size Subarray Sum](https://leetcode.com/problems/minimum-size-subarray-sum/) `⭐`
- [ ] 🟡 [1004. Max Consecutive Ones III](https://leetcode.com/problems/max-consecutive-ones-iii/) `⭐`
- [ ] 🟡 [1493. Longest Subarray of 1's After Deleting One Element](https://leetcode.com/problems/longest-subarray-of-1s-after-deleting-one-element/)
- [ ] 🟡 [713. Subarray Product Less Than K](https://leetcode.com/problems/subarray-product-less-than-k/)
- [ ] 🟡 [904. Fruit Into Baskets](https://leetcode.com/problems/fruit-into-baskets/)
- [ ] 🟡 [1695. Maximum Erasure Value](https://leetcode.com/problems/maximum-erasure-value/)
- [ ] 🟡 [1208. Get Equal Substrings Within Budget](https://leetcode.com/problems/get-equal-substrings-within-budget/)

</details>

<details>
<summary><b>Phase 6 · Frequency Window</b> &nbsp;<sub>(5 problems)</sub></summary>

- [ ] 🔴 [76. Minimum Window Substring](https://leetcode.com/problems/minimum-window-substring/) `⭐⭐⭐⭐⭐`
- [ ] 🟡 [424. Longest Repeating Character Replacement](https://leetcode.com/problems/longest-repeating-character-replacement/) `⭐⭐⭐⭐`
- [ ] 🔴 [30. Substring with Concatenation of All Words](https://leetcode.com/problems/substring-with-concatenation-of-all-words/) `⭐⭐⭐⭐⭐`
- [ ] 🟡 [1358. Number of Substrings Containing All Three Characters](https://leetcode.com/problems/number-of-substrings-containing-all-three-characters/)
- [ ] 🟡 [438. Find All Anagrams in a String](https://leetcode.com/problems/find-all-anagrams-in-a-string/)

</details>

<details>
<summary><b>Phase 7 · At Most K</b> &nbsp;<sub>(4 problems)</sub></summary>

- [ ] 🔴 [992. Subarrays with K Different Integers](https://leetcode.com/problems/subarrays-with-k-different-integers/) `⭐⭐⭐⭐⭐`
- [ ] 🟡 [930. Binary Subarrays With Sum](https://leetcode.com/problems/binary-subarrays-with-sum/)
- [ ] 🟡 [1248. Count Number of Nice Subarrays](https://leetcode.com/problems/count-number-of-nice-subarrays/)
- [ ] 🟡 [1358. Number of Substrings Containing All Three Characters](https://leetcode.com/problems/number-of-substrings-containing-all-three-characters/)

</details>

<details>
<summary><b>Phase 8 · Monotonic Deque</b> &nbsp;<sub>(5 problems)</sub></summary>

- [ ] 🔴 [239. Sliding Window Maximum](https://leetcode.com/problems/sliding-window-maximum/) `⭐⭐⭐⭐⭐`
- [ ] 🟡 [1438. Longest Continuous Subarray With Absolute Diff Less Than or Equal to Limit](https://leetcode.com/problems/longest-continuous-subarray-with-absolute-diff-less-than-or-equal-to-limit/) `⭐⭐⭐⭐⭐`
- [ ] 🔴 [862. Shortest Subarray with Sum at Least K](https://leetcode.com/problems/shortest-subarray-with-sum-at-least-k/) `⭐⭐⭐⭐⭐`
- [ ] 🔴 [1499. Max Value of Equation](https://leetcode.com/problems/max-value-of-equation/)
- [ ] 🔴 [1425. Constrained Subsequence Sum](https://leetcode.com/problems/constrained-subsequence-sum/)

</details>

<details>
<summary><b>Phase 9 · Capstone Review</b> &nbsp;<sub>(6 problems)</sub></summary>

- [ ] 🔴 [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- [ ] 🟡 [1498. Number of Subsequences That Satisfy the Given Sum Condition](https://leetcode.com/problems/number-of-subsequences-that-satisfy-the-given-sum-condition/)
- [ ] 🔴 [30. Substring with Concatenation of All Words](https://leetcode.com/problems/substring-with-concatenation-of-all-words/)
- [ ] 🔴 [76. Minimum Window Substring](https://leetcode.com/problems/minimum-window-substring/)
- [ ] 🔴 [992. Subarrays with K Different Integers](https://leetcode.com/problems/subarrays-with-k-different-integers/)
- [ ] 🔴 [239. Sliding Window Maximum](https://leetcode.com/problems/sliding-window-maximum/)

</details>

## 🔸 Prefix Sum

`49 problems` · 🟢 8 Easy · 🟡 29 Medium · 🔴 12 Hard

<details>
<summary><b>Phase 1 · Foundation</b> &nbsp;<sub>(7 problems)</sub></summary>

- [ ] 🟢 [1480. Running Sum of 1d Array](https://leetcode.com/problems/running-sum-of-1d-array/)
- [ ] 🟢 [303. Range Sum Query - Immutable](https://leetcode.com/problems/range-sum-query-immutable/)
- [ ] 🟢 [724. Find Pivot Index](https://leetcode.com/problems/find-pivot-index/)
- [ ] 🟢 [1991. Find the Middle Index in Array](https://leetcode.com/problems/find-the-middle-index-in-array/)
- [ ] 🟢 [2574. Left and Right Sum Differences](https://leetcode.com/problems/left-and-right-sum-differences/)
- [ ] 🟢 [1588. Sum of All Odd Length Subarrays](https://leetcode.com/problems/sum-of-all-odd-length-subarrays/)
- [ ] 🟢 [1732. Find the Highest Altitude](https://leetcode.com/problems/find-the-highest-altitude/)

</details>

<details>
<summary><b>Phase 2 · + Hashmap</b> &nbsp;<sub>(6 problems)</sub></summary>

- [ ] 🟡 [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- [ ] 🟡 [974. Subarray Sums Divisible by K](https://leetcode.com/problems/subarray-sums-divisible-by-k/)
- [ ] 🟡 [525. Contiguous Array](https://leetcode.com/problems/contiguous-array/)
- [ ] 🟡 [930. Binary Subarrays With Sum](https://leetcode.com/problems/binary-subarrays-with-sum/)
- [ ] 🟡 [1248. Count Number of Nice Subarrays](https://leetcode.com/problems/count-number-of-nice-subarrays/)
- [ ] 🟡 [1590. Make Sum Divisible by P](https://leetcode.com/problems/make-sum-divisible-by-p/)

</details>

<details>
<summary><b>Phase 3 · + Modulo</b> &nbsp;<sub>(5 problems)</sub></summary>

- [ ] 🟡 [523. Continuous Subarray Sum](https://leetcode.com/problems/continuous-subarray-sum/)
- [ ] 🟡 [974. Subarray Sums Divisible by K](https://leetcode.com/problems/subarray-sums-divisible-by-k/)
- [ ] 🟡 [1590. Make Sum Divisible by P](https://leetcode.com/problems/make-sum-divisible-by-p/)
- [ ] 🟡 [2845. Count of Interesting Subarrays](https://leetcode.com/problems/count-of-interesting-subarrays/)
- [ ] 🔴 [2488. Count Subarrays With Median K](https://leetcode.com/problems/count-subarrays-with-median-k/)

</details>

<details>
<summary><b>Phase 4 · + Transformation</b> &nbsp;<sub>(5 problems)</sub></summary>

- [ ] 🟡 [525. Contiguous Array](https://leetcode.com/problems/contiguous-array/)
- [ ] 🟡 [1124. Longest Well-Performing Interval](https://leetcode.com/problems/longest-well-performing-interval/)
- [ ] 🔴 [2488. Count Subarrays With Median K](https://leetcode.com/problems/count-subarrays-with-median-k/)
- [ ] 🟡 [1546. Maximum Number of Non-Overlapping Subarrays With Sum Equals Target](https://leetcode.com/problems/maximum-number-of-non-overlapping-subarrays-with-sum-equals-target/)
- [ ] 🟡 [1442. Count Triplets That Can Form Two Arrays of Equal XOR](https://leetcode.com/problems/count-triplets-that-can-form-two-arrays-of-equal-xor/)

</details>

<details>
<summary><b>Phase 5 · 2D Prefix Sum</b> &nbsp;<sub>(5 problems)</sub></summary>

- [ ] 🟡 [1314. Matrix Block Sum](https://leetcode.com/problems/matrix-block-sum/)
- [ ] 🟡 [304. Range Sum Query 2D - Immutable](https://leetcode.com/problems/range-sum-query-2d-immutable/)
- [ ] 🔴 [1074. Number of Submatrices That Sum to Target](https://leetcode.com/problems/number-of-submatrices-that-sum-to-target/)
- [ ] 🟡 [1292. Maximum Side Length of a Square with Sum Less than or Equal to Threshold](https://leetcode.com/problems/maximum-side-length-of-a-square-with-sum-less-than-or-equal-to-threshold/)
- [ ] 🔴 [363. Max Sum of Rectangle No Larger Than K](https://leetcode.com/problems/max-sum-of-rectangle-no-larger-than-k/)

</details>

<details>
<summary><b>Phase 6 · + Binary Search</b> &nbsp;<sub>(5 problems)</sub></summary>

- [ ] 🟡 [209. Minimum Size Subarray Sum](https://leetcode.com/problems/minimum-size-subarray-sum/)
- [ ] 🔴 [862. Shortest Subarray with Sum at Least K](https://leetcode.com/problems/shortest-subarray-with-sum-at-least-k/)
- [ ] 🟢 [2389. Longest Subsequence With Limited Sum](https://leetcode.com/problems/longest-subsequence-with-limited-sum/)
- [ ] 🟡 [1170. Compare Strings by Frequency of the Smallest Character](https://leetcode.com/problems/compare-strings-by-frequency-of-the-smallest-character/)
- [ ] 🟡 [528. Random Pick with Weight](https://leetcode.com/problems/random-pick-with-weight/)

</details>

<details>
<summary><b>Phase 7 · + Monotonic Deque</b> &nbsp;<sub>(1 problems)</sub></summary>

- [ ] 🔴 [862. Shortest Subarray with Sum at Least K](https://leetcode.com/problems/shortest-subarray-with-sum-at-least-k/)

</details>

<details>
<summary><b>Phase 8 · + OrderedSet / Tree</b> &nbsp;<sub>(1 problems)</sub></summary>

- [ ] 🔴 [363. Max Sum of Rectangle No Larger Than K](https://leetcode.com/problems/max-sum-of-rectangle-no-larger-than-k/)

</details>

<details>
<summary><b>Phase 9 · + Hashmap + 2D</b> &nbsp;<sub>(1 problems)</sub></summary>

- [ ] 🔴 [1074. Number of Submatrices That Sum to Target](https://leetcode.com/problems/number-of-submatrices-that-sum-to-target/)

</details>

<details>
<summary><b>Phase 10 · + Difference Array</b> &nbsp;<sub>(3 problems)</sub></summary>

- [ ] 🟡 [1109. Corporate Flight Bookings](https://leetcode.com/problems/corporate-flight-bookings/)
- [ ] 🟡 [1094. Car Pooling](https://leetcode.com/problems/car-pooling/)
- [ ] 🟡 [2536. Increment Submatrices by One](https://leetcode.com/problems/increment-submatrices-by-one/)

</details>

<details>
<summary><b>Phase 11 · Capstone Review</b> &nbsp;<sub>(10 problems)</sub></summary>

- [ ] 🔴 [327. Count of Range Sum](https://leetcode.com/problems/count-of-range-sum/)
- [ ] 🔴 [493. Reverse Pairs](https://leetcode.com/problems/reverse-pairs/)
- [ ] 🔴 [315. Count of Smaller Numbers After Self](https://leetcode.com/problems/count-of-smaller-numbers-after-self/)
- [ ] 🔴 [1542. Find Longest Awesome Substring](https://leetcode.com/problems/find-longest-awesome-substring/)
- [ ] 🟡 [1915. Number of Wonderful Substrings](https://leetcode.com/problems/number-of-wonderful-substrings/)
- [ ] 🟡 [1524. Number of Sub-arrays With Odd Sum](https://leetcode.com/problems/number-of-sub-arrays-with-odd-sum/)
- [ ] 🟡 [1442. Count Triplets That Can Form Two Arrays of Equal XOR](https://leetcode.com/problems/count-triplets-that-can-form-two-arrays-of-equal-xor/)
- [ ] 🟡 [1171. Remove Zero Sum Consecutive Nodes from Linked List](https://leetcode.com/problems/remove-zero-sum-consecutive-nodes-from-linked-list/)
- [ ] 🟡 [2483. Minimum Penalty for a Shop](https://leetcode.com/problems/minimum-penalty-for-a-shop/)
- [ ] 🟡 [1124. Longest Well-Performing Interval](https://leetcode.com/problems/longest-well-performing-interval/)

</details>

## 🔷 Merge Intervals

`29 problems` · 🟢 3 Easy · 🟡 15 Medium · 🔴 11 Hard

<details>
<summary><b>Phase 1 · Fundamentals</b> &nbsp;<sub>(4 problems)</sub></summary>

- [ ] 🟢 [228. Summary Ranges](https://leetcode.com/problems/summary-ranges/)
- [ ] 🟢 [163. Missing Ranges](https://leetcode.com/problems/missing-ranges/)
- [ ] 🟡 [56. Merge Intervals](https://leetcode.com/problems/merge-intervals/) `⭐`
- [ ] 🟡 [57. Insert Interval](https://leetcode.com/problems/insert-interval/) `⭐`

</details>

<details>
<summary><b>Phase 2 · Overlap & Greedy</b> &nbsp;<sub>(5 problems)</sub></summary>

- [ ] 🟢 [252. Meeting Rooms](https://leetcode.com/problems/meeting-rooms/)
- [ ] 🟡 [253. Meeting Rooms II](https://leetcode.com/problems/meeting-rooms-ii/) `⭐⭐⭐⭐`
- [ ] 🟡 [435. Non-overlapping Intervals](https://leetcode.com/problems/non-overlapping-intervals/) `⭐⭐⭐`
- [ ] 🟡 [452. Minimum Number of Arrows to Burst Balloons](https://leetcode.com/problems/minimum-number-of-arrows-to-burst-balloons/) `⭐⭐⭐`
- [ ] 🟡 [1288. Remove Covered Intervals](https://leetcode.com/problems/remove-covered-intervals/)

</details>

<details>
<summary><b>Phase 3 · Interval Relationships</b> &nbsp;<sub>(3 problems)</sub></summary>

- [ ] 🟡 [986. Interval List Intersections](https://leetcode.com/problems/interval-list-intersections/) `⭐⭐⭐`
- [ ] 🟡 [763. Partition Labels](https://leetcode.com/problems/partition-labels/)
- [ ] 🟡 [1272. Remove Interval](https://leetcode.com/problems/remove-interval/)

</details>

<details>
<summary><b>Phase 4 · Scheduling</b> &nbsp;<sub>(3 problems)</sub></summary>

- [ ] 🟡 [1942. The Number of the Smallest Unoccupied Chair](https://leetcode.com/problems/the-number-of-the-smallest-unoccupied-chair/) `⭐⭐⭐⭐`
- [ ] 🔴 [2402. Meeting Rooms III](https://leetcode.com/problems/meeting-rooms-iii/) `⭐⭐⭐⭐⭐`
- [ ] 🔴 [759. Employee Free Time](https://leetcode.com/problems/employee-free-time/) `⭐⭐⭐⭐`

</details>

<details>
<summary><b>Phase 5 · Sweep Line</b> &nbsp;<sub>(3 problems)</sub></summary>

- [ ] 🟡 [1094. Car Pooling](https://leetcode.com/problems/car-pooling/)
- [ ] 🟡 [731. My Calendar II](https://leetcode.com/problems/my-calendar-ii/) `⭐⭐⭐⭐`
- [ ] 🔴 [732. My Calendar III](https://leetcode.com/problems/my-calendar-iii/) `⭐⭐⭐⭐⭐`

</details>

<details>
<summary><b>Phase 6 · Interval + Heap</b> &nbsp;<sub>(3 problems)</sub></summary>

- [ ] 🟡 [253. Meeting Rooms II](https://leetcode.com/problems/meeting-rooms-ii/)
- [ ] 🔴 [1851. Minimum Interval to Include Each Query](https://leetcode.com/problems/minimum-interval-to-include-each-query/) `⭐⭐⭐⭐⭐`
- [ ] 🔴 [759. Employee Free Time](https://leetcode.com/problems/employee-free-time/)

</details>

<details>
<summary><b>Phase 7 · Interval Coverage</b> &nbsp;<sub>(4 problems)</sub></summary>

- [ ] 🟡 [1024. Video Stitching](https://leetcode.com/problems/video-stitching/) `⭐⭐⭐⭐`
- [ ] 🔴 [1326. Minimum Number of Taps to Open to Water a Garden](https://leetcode.com/problems/minimum-number-of-taps-to-open-to-water-a-garden/) `⭐⭐⭐⭐`
- [ ] 🟡 [1272. Remove Interval](https://leetcode.com/problems/remove-interval/)
- [ ] 🔴 [715. Range Module](https://leetcode.com/problems/range-module/) `⭐⭐⭐⭐⭐`

</details>

<details>
<summary><b>Phase 8 · Capstone Review</b> &nbsp;<sub>(4 problems)</sub></summary>

- [ ] 🔴 [218. The Skyline Problem](https://leetcode.com/problems/the-skyline-problem/)
- [ ] 🔴 [391. Perfect Rectangle](https://leetcode.com/problems/perfect-rectangle/)
- [ ] 🔴 [850. Rectangle Area II](https://leetcode.com/problems/rectangle-area-ii/)
- [ ] 🔴 [699. Falling Squares](https://leetcode.com/problems/falling-squares/)

</details>

---

<p align="center"><i>133 problems · 3 patterns · built for structured, repeatable DSA practice 🚀</i></p>
