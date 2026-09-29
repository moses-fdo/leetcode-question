<div align="center">

# 🧩 DSA Pattern Mastery Roadmap
### Two Pointers & Sliding Window • Prefix Sum • Merge Intervals

<p align="center">
  <b>A comprehensive, phase-by-phase LeetCode roadmap engineered to systematically build pattern recognition from core fundamentals to advanced FAANG capstones.</b>
</p>

<p align="center">
  <a href="#at-a-glance"><img src="https://img.shields.io/badge/Total_Entries-133-3b82f6?style=for-the-badge&logo=leetcode&logoColor=white" alt="Total Entries"></a>
  <a href="#at-a-glance"><img src="https://img.shields.io/badge/Unique_Problems-110-8b5cf6?style=for-the-badge" alt="Unique Problems"></a>
  <a href="#at-a-glance"><img src="https://img.shields.io/badge/Easy-23-10b981?style=for-the-badge" alt="Easy Problems"></a>
  <a href="#at-a-glance"><img src="https://img.shields.io/badge/Medium-75-f59e0b?style=for-the-badge" alt="Medium Problems"></a>
  <a href="#at-a-glance"><img src="https://img.shields.io/badge/Hard-35-ef4444?style=for-the-badge" alt="Hard Problems"></a>
  <a href="https://moses-fdo.github.io/leetcode-question/" target="_blank" rel="noopener noreferrer"><img src="https://img.shields.io/badge/Web_Tracker-Live_App-06b6d4?style=for-the-badge&logo=safari&logoColor=white" alt="Web Tracker"></a>
</p>

<p align="center">
  <a href="https://moses-fdo.github.io/leetcode-question/" target="_blank" rel="noopener noreferrer">
    <img src="https://img.shields.io/badge/🚀_LAUNCH_LIVE_INTERACTIVE_TRACKER-0F172A?style=for-the-badge&logo=googlechrome&logoColor=38BDF8&labelColor=1E293B" alt="Launch Live Tracker" height="42">
  </a>
</p>

</div>

> [!TIP]
> ### ⚡ Interactive Web Tracker Included!
> Prefer an interactive dashboard with clickable checkboxes, progress bars, real-time title/number search, and difficulty filtering?
> 
> 👉 **<a href="https://moses-fdo.github.io/leetcode-question/" target="_blank" rel="noopener noreferrer">Launch the Live Interactive Tracker App ➔</a>** *(Opens in a new tab · Auto-saves progress to your browser)*

---

## 📑 Table of Contents

- [📊 Roadmap At a Glance](#at-a-glance)
- [🎯 Must-Do Problems (⭐⭐⭐⭐⭐ Top 10)](#must-do-problems)
- [📖 How to Use This Roadmap](#how-to-use)
- [🧠 Pattern Cheat Sheet](#cheat-sheet)
- [💻 Core Python Templates](#templates)
- [📅 Suggested 6-Week Study Plan](#study-plan)
- [🔹 Pattern 1: Two Pointers & Sliding Window (55 Problems)](#two-pointers)
- [🔸 Pattern 2: Prefix Sum (49 Problems)](#prefix-sum)
- [🔷 Pattern 3: Merge Intervals (29 Problems)](#merge-intervals)

---

<a id="at-a-glance"></a>

## 📊 Roadmap At a Glance

| Pattern | Focus Techniques | Phases | Total | 🟢 Easy | 🟡 Med | 🔴 Hard | Unique | Quick Jump |
|:---|:---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| **🔹 Two Pointers & Sliding Window** | Opposite, Fast & Slow, Fixed/Variable Window, Monotonic Deque | 9 | 55 | 12 | 31 | 12 | 49 | [Jump to Pattern ➔](#two-pointers) |
| **🔸 Prefix Sum** | Hashmap, Modulo, 2D Matrix, Difference Array, Binary Search | 11 | 49 | 8 | 29 | 12 | 40 | [Jump to Pattern ➔](#prefix-sum) |
| **🔷 Merge Intervals** | Overlaps, Greedy Intervals, Sweep Line, Heap Scheduling | 8 | 29 | 3 | 15 | 11 | 26 | [Jump to Pattern ➔](#merge-intervals) |
| **⭐ Total** | **Complete Pattern Mastery** | **28** | **133** | **23** | **75** | **35** | **110** | — |

> 💡 *Note on Spaced Repetition:* High-yield problems intentionally re-appear in multiple phases under different conceptual angles. That is why there are 133 total entries covering 110 unique LeetCode problems (23 Easy, 62 Medium, 25 Hard).

---

<a id="must-do-problems"></a>

## 🎯 Must-Do Problems (⭐⭐⭐⭐⭐)

These 10 capstone problems represent the most critical, interview-tested variations across all three patterns. Every problem link opens in a separate tab:

| # | Problem | Difficulty | Pattern | Key Technique & Core Insight |
|:---:|:---|:---:|:---|:---|
| 30 | <a href="https://leetcode.com/problems/substring-with-concatenation-of-all-words/" target="_blank" rel="noopener noreferrer">**Substring with Concatenation of All Words**</a> | 🔴 Hard | Two Pointers | Multi-word sliding window tracking word counts in steps of word length |
| 76 | <a href="https://leetcode.com/problems/minimum-window-substring/" target="_blank" rel="noopener noreferrer">**Minimum Window Substring**</a> | 🔴 Hard | Two Pointers | Variable sliding window tracking character frequencies with valid match counter |
| 239 | <a href="https://leetcode.com/problems/sliding-window-maximum/" target="_blank" rel="noopener noreferrer">**Sliding Window Maximum**</a> | 🔴 Hard | Two Pointers | Monotonic decreasing deque maintaining indices within window for $O(1)$ query |
| 715 | <a href="https://leetcode.com/problems/range-module/" target="_blank" rel="noopener noreferrer">**Range Module**</a> | 🔴 Hard | Merge Intervals | Dynamic interval tracking with interval slicing, insertion, and bisect |
| 732 | <a href="https://leetcode.com/problems/my-calendar-iii/" target="_blank" rel="noopener noreferrer">**My Calendar III**</a> | 🔴 Hard | Merge Intervals | Sweep line / difference map with `+1` on start and `-1` on end to find peak k-overlap |
| 862 | <a href="https://leetcode.com/problems/shortest-subarray-with-sum-at-least-k/" target="_blank" rel="noopener noreferrer">**Shortest Subarray with Sum at Least K**</a> | 🔴 Hard | Prefix Sum | Prefix sum + monotonic increasing deque handling negative array values in $O(N)$ |
| 992 | <a href="https://leetcode.com/problems/subarrays-with-k-different-integers/" target="_blank" rel="noopener noreferrer">**Subarrays with K Different Integers**</a> | 🔴 Hard | Two Pointers | "At most K" reduction trick: `count(exact K) = atMost(K) - atMost(K - 1)` |
| 1438 | <a href="https://leetcode.com/problems/longest-continuous-subarray-with-absolute-diff-less-than-or-equal-to-limit/" target="_blank" rel="noopener noreferrer">**Longest Continuous Subarray With Absolute Diff...**</a> | 🟡 Medium | Two Pointers | Dual monotonic deques (min and max) maintaining valid sliding window bounds |
| 1851 | <a href="https://leetcode.com/problems/minimum-interval-to-include-each-query/" target="_blank" rel="noopener noreferrer">**Minimum Interval to Include Each Query**</a> | 🔴 Hard | Merge Intervals | Offline queries sorted with intervals + min-heap storing active interval lengths |
| 2402 | <a href="https://leetcode.com/problems/meeting-rooms-iii/" target="_blank" rel="noopener noreferrer">**Meeting Rooms III**</a> | 🔴 Hard | Merge Intervals | Dual priority heaps (`available_rooms` by index, `busy_rooms` by finish time) |

---

<a id="how-to-use"></a>

## 📖 How to Use This Roadmap

1. **Sequential Progression**: Solve problems top-to-bottom within each phase. Each phase isolates a specific cognitive twist on the pattern.
2. **Tab Preservation**: All problem links use `target="_blank"` to open directly on LeetCode in a new tab without losing your place in this roadmap.
3. **Spaced Repetition (`🔁`)**: When you encounter `🔁`, the problem was previously introduced under another angle. Re-solve it to cement cross-pattern recognition.
4. **Interactive Tracking**: Check off boxes here in markdown or open the **<a href="https://moses-fdo.github.io/leetcode-question/" target="_blank" rel="noopener noreferrer">Interactive Web Tracker</a>** for instant localStorage progress syncing.

### 🏷️ Legend & Priority System

| Symbol | Category | Description |
|:---:|:---:|:---|
| 🟢 | **Easy** | Foundational mechanics; focus on zero bugs and clean syntax |
| 🟡 | **Medium** | Standard interview tier; requires identifying window or state transitions |
| 🔴 | **Hard** | Capstone problems; combines multiple patterns or data structures |
| ⭐ | **Core** | Intuition-builder; 1 solid pass is sufficient |
| ⭐⭐⭐ | **Important** | High frequency; revisit and re-solve without hints after 1 week |
| ⭐⭐⭐⭐⭐ | **Critical** | Top interview must-knows; be able to code cleanly and explain time/space cold |
| 🔁 | **Repeat** | Intentional spaced repetition across phases |

---

<a id="cheat-sheet"></a>

## 🧠 Pattern Cheat Sheet

| Pattern | Recognize When (Problem Cues) | Core Invariant & Strategy | Target Complexity |
|:---|:---|:---|:---:|
| **Two Pointers (Opposite)** | Sorted array, pair/triplet target sums, palindromes | Squeeze pointers inward based on `nums[l] + nums[r]` comparison | $O(N)$ time · $O(1)$ space |
| **Fast & Slow Pointers** | Cycles in lists/arrays, middle node, duplicate finding | Floyd's cycle detection; two speeds guaranteed to intersect if cycle exists | $O(N)$ time · $O(1)$ space |
| **Fixed Sliding Window** | Subarray or substring of fixed size $K$ | Add `nums[r]`, drop `nums[l]`, slide window of size $K$ continuously | $O(N)$ time · $O(1)$ space |
| **Variable Sliding Window** | Longest or shortest valid subarray/substring | Expand `r`; while invalid, shrink `l` until window property is restored | $O(N)$ time · $O(1)$ or $O(K)$ space |
| **At Most K Trick** | "Count subarrays with exactly $K$ distinct elements or sum" | Transform to: `count(exact K) = atMost(K) - atMost(K - 1)` | $O(N)$ time · $O(K)$ space |
| **Monotonic Deque** | Window min/max queries, max sum with distance constraint | Maintain elements in monotonic order; discard candidates that cannot win | $O(N)$ time · $O(K)$ space |
| **Prefix Sum + Hashmap** | Count or find subarrays with sum equal to $K$ | `sum(i..j) = P[j] - P[i-1]`; check if `P[j] - K` exists in prefix frequency map | $O(N)$ time · $O(N)$ space |
| **Prefix Sum + Modulo** | Subarray sum divisibility by $K$ | Identical remainders `P[j] % K == P[i-1] % K` bound a divisible range | $O(N)$ time · $O(K)$ space |
| **2D Prefix Sum** | Submatrix / rectangle range sum queries | Inclusion-exclusion principle on bounding corners in $O(1)$ per query | $O(MN)$ prep · $O(1)$ query |
| **Difference Array** | Multiple range increment updates $[l, r] += v$, single final read | Range update: `diff[l] += v`, `diff[r+1] -= v`; reconstruct via prefix sum | $O(1)$ update · $O(N)$ read |
| **Merge Intervals** | Overlapping intervals, interval union, insertion | Sort by start time; if `start <= last_end`, merge; else push new interval | $O(N \log N)$ time · $O(N)$ space |
| **Greedy Intervals** | Maximum non-overlapping intervals, minimum arrows/cuts | Sort by end time; greedily pick interval finishing earliest to maximize room | $O(N \log N)$ time · $O(1)$ space |
| **Sweep Line** | Peak concurrent active events, room booking count | Decompose intervals into `(start, +1)` and `(end, -1)` points; sort and scan | $O(N \log N)$ time · $O(N)$ space |
| **Interval + Heap** | Room assignment by index, meeting schedules | Min-heap tracks currently active allocations by finish time; free on expire | $O(N \log N)$ time · $O(N)$ space |

---

<a id="templates"></a>

## 💻 Core Python Templates

<details>
<summary><b>Click to expand 6 Essential Pattern Code Templates</b></summary>
<br>

### 1. Opposite Direction Two Pointers
```python
def two_sum_sorted(nums: list[int], target: int) -> list[int]:
    left, right = 0, len(nums) - 1
    while left < right:
        curr = nums[left] + nums[right]
        if curr == target:
            return [left + 1, right + 1]
        elif curr < target:
            left += 1
        else:
            right -= 1
    return []
```

### 2. Variable Sliding Window (Longest Valid Subarray)
```python
def longest_valid_window(nums: list[int]) -> int:
    left = max_len = 0
    state = {}  # or frequency map
    for right, val in enumerate(nums):
        add_to_state(val)
        while not is_valid():
            remove_from_state(nums[left])
            left += 1
        max_len = max(max_len, right - left + 1)
    return max_len
```

### 3. Variable Sliding Window (Shortest Valid Subarray)
```python
def min_subarray_len(target: int, nums: list[int]) -> int:
    left = 0
    curr_sum = 0
    min_len = float('inf')
    for right, val in enumerate(nums):
        curr_sum += val
        while curr_sum >= target:
            min_len = min(min_len, right - left + 1)
            curr_sum -= nums[left]
            left += 1
    return min_len if min_len != float('inf') else 0
```

### 4. Prefix Sum + Hashmap (Count Subarrays Sum == K)
```python
def subarray_sum(nums: list[int], k: int) -> int:
    prefix_counts = {0: 1}  # base case: empty prefix sum is 0
    curr_sum = count = 0
    for x in nums:
        curr_sum += x
        count += prefix_counts.get(curr_sum - k, 0)
        prefix_counts[curr_sum] = prefix_counts.get(curr_sum, 0) + 1
    return count
```

### 5. Merge Intervals
```python
def merge_intervals(intervals: list[list[int]]) -> list[list[int]]:
    if not intervals:
        return []
    intervals.sort(key=lambda x: x[0])
    merged = [intervals[0]]
    for start, end in intervals[1:]:
        if start <= merged[-1][1]:
            merged[-1][1] = max(merged[-1][1], end)
        else:
            merged.append([start, end])
    return merged
```

### 6. Sweep Line Algorithm (Maximum Concurrent Events)
```python
def max_concurrent_events(intervals: list[list[int]]) -> int:
    events = []
    for start, end in intervals:
        events.append((start, 1))   # event begins
        events.append((end, -1))    # event ends
    # sort by time; if times tie, ends (-1) before starts (1) if non-overlapping
    events.sort(key=lambda x: (x[0], x[1]))
    
    max_active = curr_active = 0
    for _, delta in events:
        curr_active += delta
        max_active = max(max_active, curr_active)
    return max_active
```

</details>

---

<a id="study-plan"></a>

## 📅 Suggested 6-Week Study Plan

| Week | Focus Area | Recommended Target | Goal & Checkpoint |
|:---:|:---|:---|:---|
| **Week 1** | **Two Pointers Foundations** | Two Pointers Phases 1–3 (21 problems) | Master opposite pointers, cycle detection, and in-place manipulation |
| **Week 2** | **Sliding Window Mechanics** | Two Pointers Phases 4–7 (23 problems) | Master fixed and variable windows, frequency maps, and the "At Most K" trick |
| **Week 3** | **Monotonic Deques & Prefix Basics** | Two Pointers Phases 8–9 + Prefix Sum Phases 1–4 (29 problems) | Solve Sliding Window Maximum and master prefix sum with hashmap lookups |
| **Week 4** | **Prefix Sum Deep Dive** | Prefix Sum Phases 5–11 (26 problems) | Conquer 2D prefix sums, difference arrays, and binary search bounds |
| **Week 5** | **Interval Foundations & Greedy** | Merge Intervals Phases 1–5 (18 problems) | Master interval sorting, overlap conditions, and sweep line algorithms |
| **Week 6** | **Interval Heaps, Coverage & Capstones** | Merge Intervals Phases 6–8 + Re-solve ⭐⭐⭐⭐⭐ (11+ problems) | Master heap-based scheduling and complete all 10 critical capstones cold |

---

<a id="two-pointers"></a>

## 🔹 Two Pointers & Sliding Window

`55 problems` · 🟢 12 Easy · 🟡 31 Medium · 🔴 12 Hard

<div align="center">

**Quick Jump to Phase:**  
[1. Fundamentals](#tp-p1) • [2. Opposite Pointers](#tp-p2) • [3. Fast & Slow Pointers](#tp-p3) • [4. Fixed Sliding Window](#tp-p4) • [5. Variable Sliding Window](#tp-p5)  
[6. Frequency Window](#tp-p6) • [7. At Most K](#tp-p7) • [8. Monotonic Deque](#tp-p8) • [9. Capstone Review](#tp-p9)  

</div>

<a id="tp-p1"></a>
<details open>
<summary><b>Phase 1 · Fundamentals</b> &nbsp;<sub>(8 problems · 🟢 7 Easy · 🟡 1 Med)</sub></summary>
<br>

| Status | # | Problem | Difficulty | Priority | Topic Tags | Notes |
|:---:|:---:|:---|:---:|:---:|:---|:---|
| [ ] | `344` | <a href="https://leetcode.com/problems/reverse-string/" target="_blank" rel="noopener noreferrer"><b>Reverse String</b></a> | 🟢 Easy | — | `Two Pointers` `String` | — |
| [ ] | `125` | <a href="https://leetcode.com/problems/valid-palindrome/" target="_blank" rel="noopener noreferrer"><b>Valid Palindrome</b></a> | 🟢 Easy | — | `Two Pointers` `String` | — |
| [ ] | `167` | <a href="https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/" target="_blank" rel="noopener noreferrer"><b>Two Sum II - Input Array Is Sorted</b></a> | 🟡 Medium | — | `Array` `Two Pointers` | — |
| [ ] | `283` | <a href="https://leetcode.com/problems/move-zeroes/" target="_blank" rel="noopener noreferrer"><b>Move Zeroes</b></a> | 🟢 Easy | — | `Array` `Two Pointers` | — |
| [ ] | `26` | <a href="https://leetcode.com/problems/remove-duplicates-from-sorted-array/" target="_blank" rel="noopener noreferrer"><b>Remove Duplicates from Sorted Array</b></a> | 🟢 Easy | — | `Array` `Two Pointers` | — |
| [ ] | `27` | <a href="https://leetcode.com/problems/remove-element/" target="_blank" rel="noopener noreferrer"><b>Remove Element</b></a> | 🟢 Easy | — | `Array` `Two Pointers` | — |
| [ ] | `977` | <a href="https://leetcode.com/problems/squares-of-a-sorted-array/" target="_blank" rel="noopener noreferrer"><b>Squares of a Sorted Array</b></a> | 🟢 Easy | — | `Array` `Two Pointers` | — |
| [ ] | `88` | <a href="https://leetcode.com/problems/merge-sorted-array/" target="_blank" rel="noopener noreferrer"><b>Merge Sorted Array</b></a> | 🟢 Easy | — | `Array` `Two Pointers` | — |

</details>

<a id="tp-p2"></a>
<details open>
<summary><b>Phase 2 · Opposite Pointers</b> &nbsp;<sub>(7 problems · 🟡 7 Med)</sub></summary>
<br>

| Status | # | Problem | Difficulty | Priority | Topic Tags | Notes |
|:---:|:---:|:---|:---:|:---:|:---|:---|
| [ ] | `11` | <a href="https://leetcode.com/problems/container-with-most-water/" target="_blank" rel="noopener noreferrer"><b>Container With Most Water</b></a> | 🟡 Medium | — | `Array` `Two Pointers` | — |
| [ ] | `15` | <a href="https://leetcode.com/problems/3sum/" target="_blank" rel="noopener noreferrer"><b>3Sum</b></a> | 🟡 Medium | — | `Array` `Two Pointers` | — |
| [ ] | `16` | <a href="https://leetcode.com/problems/3sum-closest/" target="_blank" rel="noopener noreferrer"><b>3Sum Closest</b></a> | 🟡 Medium | — | `Array` `Two Pointers` | — |
| [ ] | `18` | <a href="https://leetcode.com/problems/4sum/" target="_blank" rel="noopener noreferrer"><b>4Sum</b></a> | 🟡 Medium | — | `Array` `Two Pointers` | — |
| [ ] | `259` | <a href="https://leetcode.com/problems/3sum-smaller/" target="_blank" rel="noopener noreferrer"><b>3Sum Smaller</b></a> | 🟡 Medium | — | `Array` `Two Pointers` | — |
| [ ] | `611` | <a href="https://leetcode.com/problems/valid-triangle-number/" target="_blank" rel="noopener noreferrer"><b>Valid Triangle Number</b></a> | 🟡 Medium | — | `Array` `Two Pointers` | — |
| [ ] | `881` | <a href="https://leetcode.com/problems/boats-to-save-people/" target="_blank" rel="noopener noreferrer"><b>Boats to Save People</b></a> | 🟡 Medium | — | `Array` `Two Pointers` | — |

</details>

<a id="tp-p3"></a>
<details open>
<summary><b>Phase 3 · Fast & Slow Pointers</b> &nbsp;<sub>(6 problems · 🟢 3 Easy · 🟡 3 Med)</sub></summary>
<br>

| Status | # | Problem | Difficulty | Priority | Topic Tags | Notes |
|:---:|:---:|:---|:---:|:---:|:---|:---|
| [ ] | `141` | <a href="https://leetcode.com/problems/linked-list-cycle/" target="_blank" rel="noopener noreferrer"><b>Linked List Cycle</b></a> | 🟢 Easy | — | `Hash Table` `Linked List` | — |
| [ ] | `142` | <a href="https://leetcode.com/problems/linked-list-cycle-ii/" target="_blank" rel="noopener noreferrer"><b>Linked List Cycle II</b></a> | 🟡 Medium | — | `Hash Table` `Linked List` | — |
| [ ] | `876` | <a href="https://leetcode.com/problems/middle-of-the-linked-list/" target="_blank" rel="noopener noreferrer"><b>Middle of the Linked List</b></a> | 🟢 Easy | — | `Linked List` `Two Pointers` | — |
| [ ] | `202` | <a href="https://leetcode.com/problems/happy-number/" target="_blank" rel="noopener noreferrer"><b>Happy Number</b></a> | 🟢 Easy | — | `Hash Table` `Math` | — |
| [ ] | `287` | <a href="https://leetcode.com/problems/find-the-duplicate-number/" target="_blank" rel="noopener noreferrer"><b>Find the Duplicate Number</b></a> | 🟡 Medium | — | `Array` `Two Pointers` | — |
| [ ] | `457` | <a href="https://leetcode.com/problems/circular-array-loop/" target="_blank" rel="noopener noreferrer"><b>Circular Array Loop</b></a> | 🟡 Medium | — | `Array` `Hash Table` | — |

</details>

<a id="tp-p4"></a>
<details open>
<summary><b>Phase 4 · Fixed Sliding Window</b> &nbsp;<sub>(6 problems · 🟢 1 Easy · 🟡 5 Med)</sub></summary>
<br>

| Status | # | Problem | Difficulty | Priority | Topic Tags | Notes |
|:---:|:---:|:---|:---:|:---:|:---|:---|
| [ ] | `643` | <a href="https://leetcode.com/problems/maximum-average-subarray-i/" target="_blank" rel="noopener noreferrer"><b>Maximum Average Subarray I</b></a> | 🟢 Easy | — | `Array` `Sliding Window` | — |
| [ ] | `1343` | <a href="https://leetcode.com/problems/number-of-sub-arrays-of-size-k-and-average-greater-than-or-equal-to-threshold/" target="_blank" rel="noopener noreferrer"><b>Number of Sub-arrays of Size K and Average Greater than or Equal to Threshold</b></a> | 🟡 Medium | — | `Array` `Sliding Window` | — |
| [ ] | `1456` | <a href="https://leetcode.com/problems/maximum-number-of-vowels-in-a-substring-of-given-length/" target="_blank" rel="noopener noreferrer"><b>Maximum Number of Vowels in a Substring of Given Length</b></a> | 🟡 Medium | — | `String` `Sliding Window` | — |
| [ ] | `1052` | <a href="https://leetcode.com/problems/grumpy-bookstore-owner/" target="_blank" rel="noopener noreferrer"><b>Grumpy Bookstore Owner</b></a> | 🟡 Medium | — | `Array` `Sliding Window` | — |
| [ ] | `567` | <a href="https://leetcode.com/problems/permutation-in-string/" target="_blank" rel="noopener noreferrer"><b>Permutation in String</b></a> | 🟡 Medium | ⭐ Core | `Hash Table` `Two Pointers` | — |
| [ ] | `438` | <a href="https://leetcode.com/problems/find-all-anagrams-in-a-string/" target="_blank" rel="noopener noreferrer"><b>Find All Anagrams in a String</b></a> | 🟡 Medium | ⭐ Core | `Hash Table` `String` | — |

</details>

<a id="tp-p5"></a>
<details open>
<summary><b>Phase 5 · Variable Sliding Window</b> &nbsp;<sub>(8 problems · 🟢 1 Easy · 🟡 7 Med)</sub></summary>
<br>

| Status | # | Problem | Difficulty | Priority | Topic Tags | Notes |
|:---:|:---:|:---|:---:|:---:|:---|:---|
| [ ] | `28` | <a href="https://leetcode.com/problems/find-the-index-of-the-first-occurrence-in-a-string/" target="_blank" rel="noopener noreferrer"><b>Find the Index of the First Occurrence in a String</b></a> | 🟢 Easy | ⭐⭐⭐ Important | `Two Pointers` `String` | — |
| [ ] | `209` | <a href="https://leetcode.com/problems/minimum-size-subarray-sum/" target="_blank" rel="noopener noreferrer"><b>Minimum Size Subarray Sum</b></a> | 🟡 Medium | ⭐ Core | `Array` `Binary Search` | — |
| [ ] | `1004` | <a href="https://leetcode.com/problems/max-consecutive-ones-iii/" target="_blank" rel="noopener noreferrer"><b>Max Consecutive Ones III</b></a> | 🟡 Medium | ⭐ Core | `Array` `Binary Search` | — |
| [ ] | `1493` | <a href="https://leetcode.com/problems/longest-subarray-of-1s-after-deleting-one-element/" target="_blank" rel="noopener noreferrer"><b>Longest Subarray of 1's After Deleting One Element</b></a> | 🟡 Medium | — | `Array` `Dynamic Programming` | — |
| [ ] | `713` | <a href="https://leetcode.com/problems/subarray-product-less-than-k/" target="_blank" rel="noopener noreferrer"><b>Subarray Product Less Than K</b></a> | 🟡 Medium | — | `Array` `Binary Search` | — |
| [ ] | `904` | <a href="https://leetcode.com/problems/fruit-into-baskets/" target="_blank" rel="noopener noreferrer"><b>Fruit Into Baskets</b></a> | 🟡 Medium | — | `Array` `Hash Table` | — |
| [ ] | `1695` | <a href="https://leetcode.com/problems/maximum-erasure-value/" target="_blank" rel="noopener noreferrer"><b>Maximum Erasure Value</b></a> | 🟡 Medium | — | `Array` `Hash Table` | — |
| [ ] | `1208` | <a href="https://leetcode.com/problems/get-equal-substrings-within-budget/" target="_blank" rel="noopener noreferrer"><b>Get Equal Substrings Within Budget</b></a> | 🟡 Medium | — | `String` `Binary Search` | — |

</details>

<a id="tp-p6"></a>
<details open>
<summary><b>Phase 6 · Frequency Window</b> &nbsp;<sub>(5 problems · 🟡 3 Med · 🔴 2 Hard)</sub></summary>
<br>

| Status | # | Problem | Difficulty | Priority | Topic Tags | Notes |
|:---:|:---:|:---|:---:|:---:|:---|:---|
| [ ] | `76` | <a href="https://leetcode.com/problems/minimum-window-substring/" target="_blank" rel="noopener noreferrer"><b>Minimum Window Substring</b></a> | 🔴 Hard | ⭐⭐⭐⭐⭐ Critical | `Hash Table` `String` | 🎯 Capstone |
| [ ] | `424` | <a href="https://leetcode.com/problems/longest-repeating-character-replacement/" target="_blank" rel="noopener noreferrer"><b>Longest Repeating Character Replacement</b></a> | 🟡 Medium | ⭐⭐⭐⭐ Essential | `Hash Table` `String` | — |
| [ ] | `30` | <a href="https://leetcode.com/problems/substring-with-concatenation-of-all-words/" target="_blank" rel="noopener noreferrer"><b>Substring with Concatenation of All Words</b></a> | 🔴 Hard | ⭐⭐⭐⭐⭐ Critical | `Hash Table` `String` | 🎯 Capstone |
| [ ] | `1358` | <a href="https://leetcode.com/problems/number-of-substrings-containing-all-three-characters/" target="_blank" rel="noopener noreferrer"><b>Number of Substrings Containing All Three Characters</b></a> | 🟡 Medium | — | `Hash Table` `String` | — |
| [ ] | `438` | <a href="https://leetcode.com/problems/find-all-anagrams-in-a-string/" target="_blank" rel="noopener noreferrer"><b>Find All Anagrams in a String</b></a> | 🟡 Medium | — | `Hash Table` `String` | 🔁 Spaced Repetition |

</details>

<a id="tp-p7"></a>
<details open>
<summary><b>Phase 7 · At Most K</b> &nbsp;<sub>(4 problems · 🟡 3 Med · 🔴 1 Hard)</sub></summary>
<br>

| Status | # | Problem | Difficulty | Priority | Topic Tags | Notes |
|:---:|:---:|:---|:---:|:---:|:---|:---|
| [ ] | `992` | <a href="https://leetcode.com/problems/subarrays-with-k-different-integers/" target="_blank" rel="noopener noreferrer"><b>Subarrays with K Different Integers</b></a> | 🔴 Hard | ⭐⭐⭐⭐⭐ Critical | `Array` `Hash Table` | 🎯 Capstone |
| [ ] | `930` | <a href="https://leetcode.com/problems/binary-subarrays-with-sum/" target="_blank" rel="noopener noreferrer"><b>Binary Subarrays With Sum</b></a> | 🟡 Medium | — | `Array` `Hash Table` | — |
| [ ] | `1248` | <a href="https://leetcode.com/problems/count-number-of-nice-subarrays/" target="_blank" rel="noopener noreferrer"><b>Count Number of Nice Subarrays</b></a> | 🟡 Medium | — | `Array` `Hash Table` | — |
| [ ] | `1358` | <a href="https://leetcode.com/problems/number-of-substrings-containing-all-three-characters/" target="_blank" rel="noopener noreferrer"><b>Number of Substrings Containing All Three Characters</b></a> | 🟡 Medium | — | `Hash Table` `String` | 🔁 Spaced Repetition |

</details>

<a id="tp-p8"></a>
<details open>
<summary><b>Phase 8 · Monotonic Deque</b> &nbsp;<sub>(5 problems · 🟡 1 Med · 🔴 4 Hard)</sub></summary>
<br>

| Status | # | Problem | Difficulty | Priority | Topic Tags | Notes |
|:---:|:---:|:---|:---:|:---:|:---|:---|
| [ ] | `239` | <a href="https://leetcode.com/problems/sliding-window-maximum/" target="_blank" rel="noopener noreferrer"><b>Sliding Window Maximum</b></a> | 🔴 Hard | ⭐⭐⭐⭐⭐ Critical | `Array` `Queue` | 🎯 Capstone |
| [ ] | `1438` | <a href="https://leetcode.com/problems/longest-continuous-subarray-with-absolute-diff-less-than-or-equal-to-limit/" target="_blank" rel="noopener noreferrer"><b>Longest Continuous Subarray With Absolute Diff Less Than or Equal to Limit</b></a> | 🟡 Medium | ⭐⭐⭐⭐⭐ Critical | `Array` `Queue` | 🎯 Capstone |
| [ ] | `862` | <a href="https://leetcode.com/problems/shortest-subarray-with-sum-at-least-k/" target="_blank" rel="noopener noreferrer"><b>Shortest Subarray with Sum at Least K</b></a> | 🔴 Hard | ⭐⭐⭐⭐⭐ Critical | `Array` `Binary Search` | 🎯 Capstone |
| [ ] | `1499` | <a href="https://leetcode.com/problems/max-value-of-equation/" target="_blank" rel="noopener noreferrer"><b>Max Value of Equation</b></a> | 🔴 Hard | — | `Array` `Queue` | — |
| [ ] | `1425` | <a href="https://leetcode.com/problems/constrained-subsequence-sum/" target="_blank" rel="noopener noreferrer"><b>Constrained Subsequence Sum</b></a> | 🔴 Hard | — | `Array` `Dynamic Programming` | — |

</details>

<a id="tp-p9"></a>
<details open>
<summary><b>Phase 9 · Capstone Review</b> &nbsp;<sub>(6 problems · 🟡 1 Med · 🔴 5 Hard)</sub></summary>
<br>

| Status | # | Problem | Difficulty | Priority | Topic Tags | Notes |
|:---:|:---:|:---|:---:|:---:|:---|:---|
| [ ] | `42` | <a href="https://leetcode.com/problems/trapping-rain-water/" target="_blank" rel="noopener noreferrer"><b>Trapping Rain Water</b></a> | 🔴 Hard | — | `Array` `Two Pointers` | — |
| [ ] | `1498` | <a href="https://leetcode.com/problems/number-of-subsequences-that-satisfy-the-given-sum-condition/" target="_blank" rel="noopener noreferrer"><b>Number of Subsequences That Satisfy the Given Sum Condition</b></a> | 🟡 Medium | — | `Array` `Two Pointers` | — |
| [ ] | `30` | <a href="https://leetcode.com/problems/substring-with-concatenation-of-all-words/" target="_blank" rel="noopener noreferrer"><b>Substring with Concatenation of All Words</b></a> | 🔴 Hard | — | `Hash Table` `String` | 🔁 Spaced Repetition |
| [ ] | `76` | <a href="https://leetcode.com/problems/minimum-window-substring/" target="_blank" rel="noopener noreferrer"><b>Minimum Window Substring</b></a> | 🔴 Hard | — | `Hash Table` `String` | 🔁 Spaced Repetition |
| [ ] | `992` | <a href="https://leetcode.com/problems/subarrays-with-k-different-integers/" target="_blank" rel="noopener noreferrer"><b>Subarrays with K Different Integers</b></a> | 🔴 Hard | — | `Array` `Hash Table` | 🔁 Spaced Repetition |
| [ ] | `239` | <a href="https://leetcode.com/problems/sliding-window-maximum/" target="_blank" rel="noopener noreferrer"><b>Sliding Window Maximum</b></a> | 🔴 Hard | — | `Array` `Queue` | 🔁 Spaced Repetition |

</details>


<a id="prefix-sum"></a>

## 🔸 Prefix Sum

`49 problems` · 🟢 8 Easy · 🟡 29 Medium · 🔴 12 Hard

<div align="center">

**Quick Jump to Phase:**  
[1. Foundation](#ps-p1) • [2. + Hashmap](#ps-p2) • [3. + Modulo](#ps-p3) • [4. + Transformation](#ps-p4) • [5. 2D Prefix Sum](#ps-p5)  
[6. + Binary Search](#ps-p6) • [7. + Monotonic Deque](#ps-p7) • [8. + OrderedSet / Tree](#ps-p8) • [9. + Hashmap + 2D](#ps-p9) • [10. + Difference Array](#ps-p10)  
[11. Capstone Review](#ps-p11)  

</div>

<a id="ps-p1"></a>
<details open>
<summary><b>Phase 1 · Foundation</b> &nbsp;<sub>(7 problems · 🟢 7 Easy)</sub></summary>
<br>

| Status | # | Problem | Difficulty | Priority | Topic Tags | Notes |
|:---:|:---:|:---|:---:|:---:|:---|:---|
| [ ] | `1480` | <a href="https://leetcode.com/problems/running-sum-of-1d-array/" target="_blank" rel="noopener noreferrer"><b>Running Sum of 1d Array</b></a> | 🟢 Easy | — | `Array` `Prefix Sum` | — |
| [ ] | `303` | <a href="https://leetcode.com/problems/range-sum-query-immutable/" target="_blank" rel="noopener noreferrer"><b>Range Sum Query - Immutable</b></a> | 🟢 Easy | — | `Array` `Design` | — |
| [ ] | `724` | <a href="https://leetcode.com/problems/find-pivot-index/" target="_blank" rel="noopener noreferrer"><b>Find Pivot Index</b></a> | 🟢 Easy | — | `Array` `Prefix Sum` | — |
| [ ] | `1991` | <a href="https://leetcode.com/problems/find-the-middle-index-in-array/" target="_blank" rel="noopener noreferrer"><b>Find the Middle Index in Array</b></a> | 🟢 Easy | — | `Array` `Prefix Sum` | — |
| [ ] | `2574` | <a href="https://leetcode.com/problems/left-and-right-sum-differences/" target="_blank" rel="noopener noreferrer"><b>Left and Right Sum Differences</b></a> | 🟢 Easy | — | `Array` `Prefix Sum` | — |
| [ ] | `1588` | <a href="https://leetcode.com/problems/sum-of-all-odd-length-subarrays/" target="_blank" rel="noopener noreferrer"><b>Sum of All Odd Length Subarrays</b></a> | 🟢 Easy | — | `Array` `Math` | — |
| [ ] | `1732` | <a href="https://leetcode.com/problems/find-the-highest-altitude/" target="_blank" rel="noopener noreferrer"><b>Find the Highest Altitude</b></a> | 🟢 Easy | — | `Array` `Prefix Sum` | — |

</details>

<a id="ps-p2"></a>
<details open>
<summary><b>Phase 2 · + Hashmap</b> &nbsp;<sub>(6 problems · 🟡 6 Med)</sub></summary>
<br>

| Status | # | Problem | Difficulty | Priority | Topic Tags | Notes |
|:---:|:---:|:---|:---:|:---:|:---|:---|
| [ ] | `560` | <a href="https://leetcode.com/problems/subarray-sum-equals-k/" target="_blank" rel="noopener noreferrer"><b>Subarray Sum Equals K</b></a> | 🟡 Medium | — | `Array` `Hash Table` | — |
| [ ] | `974` | <a href="https://leetcode.com/problems/subarray-sums-divisible-by-k/" target="_blank" rel="noopener noreferrer"><b>Subarray Sums Divisible by K</b></a> | 🟡 Medium | — | `Array` `Hash Table` | — |
| [ ] | `525` | <a href="https://leetcode.com/problems/contiguous-array/" target="_blank" rel="noopener noreferrer"><b>Contiguous Array</b></a> | 🟡 Medium | — | `Array` `Hash Table` | — |
| [ ] | `930` | <a href="https://leetcode.com/problems/binary-subarrays-with-sum/" target="_blank" rel="noopener noreferrer"><b>Binary Subarrays With Sum</b></a> | 🟡 Medium | — | `Array` `Hash Table` | — |
| [ ] | `1248` | <a href="https://leetcode.com/problems/count-number-of-nice-subarrays/" target="_blank" rel="noopener noreferrer"><b>Count Number of Nice Subarrays</b></a> | 🟡 Medium | — | `Array` `Hash Table` | — |
| [ ] | `1590` | <a href="https://leetcode.com/problems/make-sum-divisible-by-p/" target="_blank" rel="noopener noreferrer"><b>Make Sum Divisible by P</b></a> | 🟡 Medium | — | `Array` `Hash Table` | — |

</details>

<a id="ps-p3"></a>
<details open>
<summary><b>Phase 3 · + Modulo</b> &nbsp;<sub>(5 problems · 🟡 4 Med · 🔴 1 Hard)</sub></summary>
<br>

| Status | # | Problem | Difficulty | Priority | Topic Tags | Notes |
|:---:|:---:|:---|:---:|:---:|:---|:---|
| [ ] | `523` | <a href="https://leetcode.com/problems/continuous-subarray-sum/" target="_blank" rel="noopener noreferrer"><b>Continuous Subarray Sum</b></a> | 🟡 Medium | — | `Array` `Hash Table` | — |
| [ ] | `974` | <a href="https://leetcode.com/problems/subarray-sums-divisible-by-k/" target="_blank" rel="noopener noreferrer"><b>Subarray Sums Divisible by K</b></a> | 🟡 Medium | — | `Array` `Hash Table` | 🔁 Spaced Repetition |
| [ ] | `1590` | <a href="https://leetcode.com/problems/make-sum-divisible-by-p/" target="_blank" rel="noopener noreferrer"><b>Make Sum Divisible by P</b></a> | 🟡 Medium | — | `Array` `Hash Table` | 🔁 Spaced Repetition |
| [ ] | `2845` | <a href="https://leetcode.com/problems/count-of-interesting-subarrays/" target="_blank" rel="noopener noreferrer"><b>Count of Interesting Subarrays</b></a> | 🟡 Medium | — | `Array` `Hash Table` | — |
| [ ] | `2488` | <a href="https://leetcode.com/problems/count-subarrays-with-median-k/" target="_blank" rel="noopener noreferrer"><b>Count Subarrays With Median K</b></a> | 🔴 Hard | — | `Array` `Hash Table` | — |

</details>

<a id="ps-p4"></a>
<details open>
<summary><b>Phase 4 · + Transformation</b> &nbsp;<sub>(5 problems · 🟡 4 Med · 🔴 1 Hard)</sub></summary>
<br>

| Status | # | Problem | Difficulty | Priority | Topic Tags | Notes |
|:---:|:---:|:---|:---:|:---:|:---|:---|
| [ ] | `525` | <a href="https://leetcode.com/problems/contiguous-array/" target="_blank" rel="noopener noreferrer"><b>Contiguous Array</b></a> | 🟡 Medium | — | `Array` `Hash Table` | 🔁 Spaced Repetition |
| [ ] | `1124` | <a href="https://leetcode.com/problems/longest-well-performing-interval/" target="_blank" rel="noopener noreferrer"><b>Longest Well-Performing Interval</b></a> | 🟡 Medium | — | `Array` `Hash Table` | — |
| [ ] | `2488` | <a href="https://leetcode.com/problems/count-subarrays-with-median-k/" target="_blank" rel="noopener noreferrer"><b>Count Subarrays With Median K</b></a> | 🔴 Hard | — | `Array` `Hash Table` | 🔁 Spaced Repetition |
| [ ] | `1546` | <a href="https://leetcode.com/problems/maximum-number-of-non-overlapping-subarrays-with-sum-equals-target/" target="_blank" rel="noopener noreferrer"><b>Maximum Number of Non-Overlapping Subarrays With Sum Equals Target</b></a> | 🟡 Medium | — | `Array` `Hash Table` | — |
| [ ] | `1442` | <a href="https://leetcode.com/problems/count-triplets-that-can-form-two-arrays-of-equal-xor/" target="_blank" rel="noopener noreferrer"><b>Count Triplets That Can Form Two Arrays of Equal XOR</b></a> | 🟡 Medium | — | `Array` `Hash Table` | — |

</details>

<a id="ps-p5"></a>
<details open>
<summary><b>Phase 5 · 2D Prefix Sum</b> &nbsp;<sub>(5 problems · 🟡 3 Med · 🔴 2 Hard)</sub></summary>
<br>

| Status | # | Problem | Difficulty | Priority | Topic Tags | Notes |
|:---:|:---:|:---|:---:|:---:|:---|:---|
| [ ] | `1314` | <a href="https://leetcode.com/problems/matrix-block-sum/" target="_blank" rel="noopener noreferrer"><b>Matrix Block Sum</b></a> | 🟡 Medium | — | `Array` `Matrix` | — |
| [ ] | `304` | <a href="https://leetcode.com/problems/range-sum-query-2d-immutable/" target="_blank" rel="noopener noreferrer"><b>Range Sum Query 2D - Immutable</b></a> | 🟡 Medium | — | `Array` `Design` | — |
| [ ] | `1074` | <a href="https://leetcode.com/problems/number-of-submatrices-that-sum-to-target/" target="_blank" rel="noopener noreferrer"><b>Number of Submatrices That Sum to Target</b></a> | 🔴 Hard | — | `Array` `Hash Table` | — |
| [ ] | `1292` | <a href="https://leetcode.com/problems/maximum-side-length-of-a-square-with-sum-less-than-or-equal-to-threshold/" target="_blank" rel="noopener noreferrer"><b>Maximum Side Length of a Square with Sum Less than or Equal to Threshold</b></a> | 🟡 Medium | — | `Array` `Binary Search` | — |
| [ ] | `363` | <a href="https://leetcode.com/problems/max-sum-of-rectangle-no-larger-than-k/" target="_blank" rel="noopener noreferrer"><b>Max Sum of Rectangle No Larger Than K</b></a> | 🔴 Hard | — | `Array` `Binary Search` | — |

</details>

<a id="ps-p6"></a>
<details open>
<summary><b>Phase 6 · + Binary Search</b> &nbsp;<sub>(5 problems · 🟢 1 Easy · 🟡 3 Med · 🔴 1 Hard)</sub></summary>
<br>

| Status | # | Problem | Difficulty | Priority | Topic Tags | Notes |
|:---:|:---:|:---|:---:|:---:|:---|:---|
| [ ] | `209` | <a href="https://leetcode.com/problems/minimum-size-subarray-sum/" target="_blank" rel="noopener noreferrer"><b>Minimum Size Subarray Sum</b></a> | 🟡 Medium | — | `Array` `Binary Search` | — |
| [ ] | `862` | <a href="https://leetcode.com/problems/shortest-subarray-with-sum-at-least-k/" target="_blank" rel="noopener noreferrer"><b>Shortest Subarray with Sum at Least K</b></a> | 🔴 Hard | — | `Array` `Binary Search` | — |
| [ ] | `2389` | <a href="https://leetcode.com/problems/longest-subsequence-with-limited-sum/" target="_blank" rel="noopener noreferrer"><b>Longest Subsequence With Limited Sum</b></a> | 🟢 Easy | — | `Array` `Binary Search` | — |
| [ ] | `1170` | <a href="https://leetcode.com/problems/compare-strings-by-frequency-of-the-smallest-character/" target="_blank" rel="noopener noreferrer"><b>Compare Strings by Frequency of the Smallest Character</b></a> | 🟡 Medium | — | `Array` `Hash Table` | — |
| [ ] | `528` | <a href="https://leetcode.com/problems/random-pick-with-weight/" target="_blank" rel="noopener noreferrer"><b>Random Pick with Weight</b></a> | 🟡 Medium | — | `Array` `Math` | — |

</details>

<a id="ps-p7"></a>
<details open>
<summary><b>Phase 7 · + Monotonic Deque</b> &nbsp;<sub>(1 problems · 🔴 1 Hard)</sub></summary>
<br>

| Status | # | Problem | Difficulty | Priority | Topic Tags | Notes |
|:---:|:---:|:---|:---:|:---:|:---|:---|
| [ ] | `862` | <a href="https://leetcode.com/problems/shortest-subarray-with-sum-at-least-k/" target="_blank" rel="noopener noreferrer"><b>Shortest Subarray with Sum at Least K</b></a> | 🔴 Hard | — | `Array` `Binary Search` | 🔁 Spaced Repetition |

</details>

<a id="ps-p8"></a>
<details open>
<summary><b>Phase 8 · + OrderedSet / Tree</b> &nbsp;<sub>(1 problems · 🔴 1 Hard)</sub></summary>
<br>

| Status | # | Problem | Difficulty | Priority | Topic Tags | Notes |
|:---:|:---:|:---|:---:|:---:|:---|:---|
| [ ] | `363` | <a href="https://leetcode.com/problems/max-sum-of-rectangle-no-larger-than-k/" target="_blank" rel="noopener noreferrer"><b>Max Sum of Rectangle No Larger Than K</b></a> | 🔴 Hard | — | `Array` `Binary Search` | 🔁 Spaced Repetition |

</details>

<a id="ps-p9"></a>
<details open>
<summary><b>Phase 9 · + Hashmap + 2D</b> &nbsp;<sub>(1 problems · 🔴 1 Hard)</sub></summary>
<br>

| Status | # | Problem | Difficulty | Priority | Topic Tags | Notes |
|:---:|:---:|:---|:---:|:---:|:---|:---|
| [ ] | `1074` | <a href="https://leetcode.com/problems/number-of-submatrices-that-sum-to-target/" target="_blank" rel="noopener noreferrer"><b>Number of Submatrices That Sum to Target</b></a> | 🔴 Hard | — | `Array` `Hash Table` | 🔁 Spaced Repetition |

</details>

<a id="ps-p10"></a>
<details open>
<summary><b>Phase 10 · + Difference Array</b> &nbsp;<sub>(3 problems · 🟡 3 Med)</sub></summary>
<br>

| Status | # | Problem | Difficulty | Priority | Topic Tags | Notes |
|:---:|:---:|:---|:---:|:---:|:---|:---|
| [ ] | `1109` | <a href="https://leetcode.com/problems/corporate-flight-bookings/" target="_blank" rel="noopener noreferrer"><b>Corporate Flight Bookings</b></a> | 🟡 Medium | — | `Array` `Prefix Sum` | — |
| [ ] | `1094` | <a href="https://leetcode.com/problems/car-pooling/" target="_blank" rel="noopener noreferrer"><b>Car Pooling</b></a> | 🟡 Medium | — | `Array` `Sorting` | — |
| [ ] | `2536` | <a href="https://leetcode.com/problems/increment-submatrices-by-one/" target="_blank" rel="noopener noreferrer"><b>Increment Submatrices by One</b></a> | 🟡 Medium | — | `Array` `Matrix` | — |

</details>

<a id="ps-p11"></a>
<details open>
<summary><b>Phase 11 · Capstone Review</b> &nbsp;<sub>(10 problems · 🟡 6 Med · 🔴 4 Hard)</sub></summary>
<br>

| Status | # | Problem | Difficulty | Priority | Topic Tags | Notes |
|:---:|:---:|:---|:---:|:---:|:---|:---|
| [ ] | `327` | <a href="https://leetcode.com/problems/count-of-range-sum/" target="_blank" rel="noopener noreferrer"><b>Count of Range Sum</b></a> | 🔴 Hard | — | `Array` `Binary Search` | — |
| [ ] | `493` | <a href="https://leetcode.com/problems/reverse-pairs/" target="_blank" rel="noopener noreferrer"><b>Reverse Pairs</b></a> | 🔴 Hard | — | `Array` `Binary Search` | — |
| [ ] | `315` | <a href="https://leetcode.com/problems/count-of-smaller-numbers-after-self/" target="_blank" rel="noopener noreferrer"><b>Count of Smaller Numbers After Self</b></a> | 🔴 Hard | — | `Array` `Binary Search` | — |
| [ ] | `1542` | <a href="https://leetcode.com/problems/find-longest-awesome-substring/" target="_blank" rel="noopener noreferrer"><b>Find Longest Awesome Substring</b></a> | 🔴 Hard | — | `Hash Table` `String` | — |
| [ ] | `1915` | <a href="https://leetcode.com/problems/number-of-wonderful-substrings/" target="_blank" rel="noopener noreferrer"><b>Number of Wonderful Substrings</b></a> | 🟡 Medium | — | `Hash Table` `String` | — |
| [ ] | `1524` | <a href="https://leetcode.com/problems/number-of-sub-arrays-with-odd-sum/" target="_blank" rel="noopener noreferrer"><b>Number of Sub-arrays With Odd Sum</b></a> | 🟡 Medium | — | `Array` `Math` | — |
| [ ] | `1442` | <a href="https://leetcode.com/problems/count-triplets-that-can-form-two-arrays-of-equal-xor/" target="_blank" rel="noopener noreferrer"><b>Count Triplets That Can Form Two Arrays of Equal XOR</b></a> | 🟡 Medium | — | `Array` `Hash Table` | 🔁 Spaced Repetition |
| [ ] | `1171` | <a href="https://leetcode.com/problems/remove-zero-sum-consecutive-nodes-from-linked-list/" target="_blank" rel="noopener noreferrer"><b>Remove Zero Sum Consecutive Nodes from Linked List</b></a> | 🟡 Medium | — | `Hash Table` `Linked List` | — |
| [ ] | `2483` | <a href="https://leetcode.com/problems/minimum-penalty-for-a-shop/" target="_blank" rel="noopener noreferrer"><b>Minimum Penalty for a Shop</b></a> | 🟡 Medium | — | `String` `Prefix Sum` | — |
| [ ] | `1124` | <a href="https://leetcode.com/problems/longest-well-performing-interval/" target="_blank" rel="noopener noreferrer"><b>Longest Well-Performing Interval</b></a> | 🟡 Medium | — | `Array` `Hash Table` | 🔁 Spaced Repetition |

</details>


<a id="merge-intervals"></a>

## 🔷 Merge Intervals

`29 problems` · 🟢 3 Easy · 🟡 15 Medium · 🔴 11 Hard

<div align="center">

**Quick Jump to Phase:**  
[1. Fundamentals](#mi-p1) • [2. Overlap & Greedy](#mi-p2) • [3. Interval Relationships](#mi-p3) • [4. Scheduling](#mi-p4) • [5. Sweep Line](#mi-p5)  
[6. Interval + Heap](#mi-p6) • [7. Interval Coverage](#mi-p7) • [8. Capstone Review](#mi-p8)  

</div>

<a id="mi-p1"></a>
<details open>
<summary><b>Phase 1 · Fundamentals</b> &nbsp;<sub>(4 problems · 🟢 2 Easy · 🟡 2 Med)</sub></summary>
<br>

| Status | # | Problem | Difficulty | Priority | Topic Tags | Notes |
|:---:|:---:|:---|:---:|:---:|:---|:---|
| [ ] | `228` | <a href="https://leetcode.com/problems/summary-ranges/" target="_blank" rel="noopener noreferrer"><b>Summary Ranges</b></a> | 🟢 Easy | — | `Array` | — |
| [ ] | `163` | <a href="https://leetcode.com/problems/missing-ranges/" target="_blank" rel="noopener noreferrer"><b>Missing Ranges</b></a> | 🟢 Easy | — | `Array` | — |
| [ ] | `56` | <a href="https://leetcode.com/problems/merge-intervals/" target="_blank" rel="noopener noreferrer"><b>Merge Intervals</b></a> | 🟡 Medium | ⭐ Core | `Array` `Sorting` | — |
| [ ] | `57` | <a href="https://leetcode.com/problems/insert-interval/" target="_blank" rel="noopener noreferrer"><b>Insert Interval</b></a> | 🟡 Medium | ⭐ Core | `Array` | — |

</details>

<a id="mi-p2"></a>
<details open>
<summary><b>Phase 2 · Overlap & Greedy</b> &nbsp;<sub>(5 problems · 🟢 1 Easy · 🟡 4 Med)</sub></summary>
<br>

| Status | # | Problem | Difficulty | Priority | Topic Tags | Notes |
|:---:|:---:|:---|:---:|:---:|:---|:---|
| [ ] | `252` | <a href="https://leetcode.com/problems/meeting-rooms/" target="_blank" rel="noopener noreferrer"><b>Meeting Rooms</b></a> | 🟢 Easy | — | `Array` `Sorting` | — |
| [ ] | `253` | <a href="https://leetcode.com/problems/meeting-rooms-ii/" target="_blank" rel="noopener noreferrer"><b>Meeting Rooms II</b></a> | 🟡 Medium | ⭐⭐⭐⭐ Essential | `Array` `Two Pointers` | — |
| [ ] | `435` | <a href="https://leetcode.com/problems/non-overlapping-intervals/" target="_blank" rel="noopener noreferrer"><b>Non-overlapping Intervals</b></a> | 🟡 Medium | ⭐⭐⭐ Important | `Array` `Dynamic Programming` | — |
| [ ] | `452` | <a href="https://leetcode.com/problems/minimum-number-of-arrows-to-burst-balloons/" target="_blank" rel="noopener noreferrer"><b>Minimum Number of Arrows to Burst Balloons</b></a> | 🟡 Medium | ⭐⭐⭐ Important | `Array` `Greedy` | — |
| [ ] | `1288` | <a href="https://leetcode.com/problems/remove-covered-intervals/" target="_blank" rel="noopener noreferrer"><b>Remove Covered Intervals</b></a> | 🟡 Medium | — | `Array` `Sorting` | — |

</details>

<a id="mi-p3"></a>
<details open>
<summary><b>Phase 3 · Interval Relationships</b> &nbsp;<sub>(3 problems · 🟡 3 Med)</sub></summary>
<br>

| Status | # | Problem | Difficulty | Priority | Topic Tags | Notes |
|:---:|:---:|:---|:---:|:---:|:---|:---|
| [ ] | `986` | <a href="https://leetcode.com/problems/interval-list-intersections/" target="_blank" rel="noopener noreferrer"><b>Interval List Intersections</b></a> | 🟡 Medium | ⭐⭐⭐ Important | `Array` `Two Pointers` | — |
| [ ] | `763` | <a href="https://leetcode.com/problems/partition-labels/" target="_blank" rel="noopener noreferrer"><b>Partition Labels</b></a> | 🟡 Medium | — | `Hash Table` `Two Pointers` | — |
| [ ] | `1272` | <a href="https://leetcode.com/problems/remove-interval/" target="_blank" rel="noopener noreferrer"><b>Remove Interval</b></a> | 🟡 Medium | — | `Array` | — |

</details>

<a id="mi-p4"></a>
<details open>
<summary><b>Phase 4 · Scheduling</b> &nbsp;<sub>(3 problems · 🟡 1 Med · 🔴 2 Hard)</sub></summary>
<br>

| Status | # | Problem | Difficulty | Priority | Topic Tags | Notes |
|:---:|:---:|:---|:---:|:---:|:---|:---|
| [ ] | `1942` | <a href="https://leetcode.com/problems/the-number-of-the-smallest-unoccupied-chair/" target="_blank" rel="noopener noreferrer"><b>The Number of the Smallest Unoccupied Chair</b></a> | 🟡 Medium | ⭐⭐⭐⭐ Essential | `Array` `Hash Table` | — |
| [ ] | `2402` | <a href="https://leetcode.com/problems/meeting-rooms-iii/" target="_blank" rel="noopener noreferrer"><b>Meeting Rooms III</b></a> | 🔴 Hard | ⭐⭐⭐⭐⭐ Critical | `Array` `Hash Table` | 🎯 Capstone |
| [ ] | `759` | <a href="https://leetcode.com/problems/employee-free-time/" target="_blank" rel="noopener noreferrer"><b>Employee Free Time</b></a> | 🔴 Hard | ⭐⭐⭐⭐ Essential | `Array` `Sweep Line` | — |

</details>

<a id="mi-p5"></a>
<details open>
<summary><b>Phase 5 · Sweep Line</b> &nbsp;<sub>(3 problems · 🟡 2 Med · 🔴 1 Hard)</sub></summary>
<br>

| Status | # | Problem | Difficulty | Priority | Topic Tags | Notes |
|:---:|:---:|:---|:---:|:---:|:---|:---|
| [ ] | `1094` | <a href="https://leetcode.com/problems/car-pooling/" target="_blank" rel="noopener noreferrer"><b>Car Pooling</b></a> | 🟡 Medium | — | `Array` `Sorting` | — |
| [ ] | `731` | <a href="https://leetcode.com/problems/my-calendar-ii/" target="_blank" rel="noopener noreferrer"><b>My Calendar II</b></a> | 🟡 Medium | ⭐⭐⭐⭐ Essential | `Array` `Binary Search` | — |
| [ ] | `732` | <a href="https://leetcode.com/problems/my-calendar-iii/" target="_blank" rel="noopener noreferrer"><b>My Calendar III</b></a> | 🔴 Hard | ⭐⭐⭐⭐⭐ Critical | `Binary Search` `Design` | 🎯 Capstone |

</details>

<a id="mi-p6"></a>
<details open>
<summary><b>Phase 6 · Interval + Heap</b> &nbsp;<sub>(3 problems · 🟡 1 Med · 🔴 2 Hard)</sub></summary>
<br>

| Status | # | Problem | Difficulty | Priority | Topic Tags | Notes |
|:---:|:---:|:---|:---:|:---:|:---|:---|
| [ ] | `253` | <a href="https://leetcode.com/problems/meeting-rooms-ii/" target="_blank" rel="noopener noreferrer"><b>Meeting Rooms II</b></a> | 🟡 Medium | — | `Array` `Two Pointers` | 🔁 Spaced Repetition |
| [ ] | `1851` | <a href="https://leetcode.com/problems/minimum-interval-to-include-each-query/" target="_blank" rel="noopener noreferrer"><b>Minimum Interval to Include Each Query</b></a> | 🔴 Hard | ⭐⭐⭐⭐⭐ Critical | `Array` `Binary Search` | 🎯 Capstone |
| [ ] | `759` | <a href="https://leetcode.com/problems/employee-free-time/" target="_blank" rel="noopener noreferrer"><b>Employee Free Time</b></a> | 🔴 Hard | — | `Array` `Sweep Line` | 🔁 Spaced Repetition |

</details>

<a id="mi-p7"></a>
<details open>
<summary><b>Phase 7 · Interval Coverage</b> &nbsp;<sub>(4 problems · 🟡 2 Med · 🔴 2 Hard)</sub></summary>
<br>

| Status | # | Problem | Difficulty | Priority | Topic Tags | Notes |
|:---:|:---:|:---|:---:|:---:|:---|:---|
| [ ] | `1024` | <a href="https://leetcode.com/problems/video-stitching/" target="_blank" rel="noopener noreferrer"><b>Video Stitching</b></a> | 🟡 Medium | ⭐⭐⭐⭐ Essential | `Array` `Dynamic Programming` | — |
| [ ] | `1326` | <a href="https://leetcode.com/problems/minimum-number-of-taps-to-open-to-water-a-garden/" target="_blank" rel="noopener noreferrer"><b>Minimum Number of Taps to Open to Water a Garden</b></a> | 🔴 Hard | ⭐⭐⭐⭐ Essential | `Array` `Dynamic Programming` | — |
| [ ] | `1272` | <a href="https://leetcode.com/problems/remove-interval/" target="_blank" rel="noopener noreferrer"><b>Remove Interval</b></a> | 🟡 Medium | — | `Array` | 🔁 Spaced Repetition |
| [ ] | `715` | <a href="https://leetcode.com/problems/range-module/" target="_blank" rel="noopener noreferrer"><b>Range Module</b></a> | 🔴 Hard | ⭐⭐⭐⭐⭐ Critical | `Design` `Segment Tree` | 🎯 Capstone |

</details>

<a id="mi-p8"></a>
<details open>
<summary><b>Phase 8 · Capstone Review</b> &nbsp;<sub>(4 problems · 🔴 4 Hard)</sub></summary>
<br>

| Status | # | Problem | Difficulty | Priority | Topic Tags | Notes |
|:---:|:---:|:---|:---:|:---:|:---|:---|
| [ ] | `218` | <a href="https://leetcode.com/problems/the-skyline-problem/" target="_blank" rel="noopener noreferrer"><b>The Skyline Problem</b></a> | 🔴 Hard | — | `Array` `Divide and Conquer` | — |
| [ ] | `391` | <a href="https://leetcode.com/problems/perfect-rectangle/" target="_blank" rel="noopener noreferrer"><b>Perfect Rectangle</b></a> | 🔴 Hard | — | `Array` `Hash Table` | — |
| [ ] | `850` | <a href="https://leetcode.com/problems/rectangle-area-ii/" target="_blank" rel="noopener noreferrer"><b>Rectangle Area II</b></a> | 🔴 Hard | — | `Array` `Segment Tree` | — |
| [ ] | `699` | <a href="https://leetcode.com/problems/falling-squares/" target="_blank" rel="noopener noreferrer"><b>Falling Squares</b></a> | 🔴 Hard | — | `Array` `Segment Tree` | — |

</details>

---

<div align="center">

<b>133 Practice Entries · 110 Unique LeetCode Problems · 3 Fundamental Patterns</b><br>
Built for structured, disciplined, and repeatable DSA interview mastery.

<br><br>

<a href="#at-a-glance">Back to Top ↑</a> &nbsp;•&nbsp; <a href="https://moses-fdo.github.io/leetcode-question/" target="_blank" rel="noopener noreferrer">Launch Interactive Web Tracker ➔</a>

</div>
