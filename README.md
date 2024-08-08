# Sliding Window - W12D1

## Problem Statement

Given two strings s and t, where s represents the main string and t represents the target characters, the goal is to find the smallest substring in s that contains all the characters of t (including duplicates). If that substring does not exist, the function returns an empty string.

## Solution Approach

The solution uses a sliding window approach, which involves two pointers representing the start and end of a window sliding over string s. The window expands by moving the end pointer to include characters until all characters from t are present. Then, the window shrinks by moving the start pointer to minimize the window size while still containing all characters from t.

## Code Design Choices

- Counter from Collections: Utilized to keep track of character frequencies in t and current window.
- Two Pointers: start and end pointers to represent window’s boundaries.
- While Loop: Checks if window contains all characters from t and to shrink window accordingly.

## Expanding and Shrinking the Window

- Expanding: window expands by incrementing end pointer and updating window_counter with each character.
- Shrinking: When all t characters are in window, the start pointer moves forward to reduce window size, updating the window_counter until a character from t is no longer in the window.

## Time and Space Complexity Analysis

- Time Complexity: O(m+n)
    m is the length of string s and n is the length of string t. Each character in s is visited at most twice, once by the end pointer and once by the start pointer.
- Space Complexity: O(m+n)
    due to required storage for two counters. In worst case, all characters of s and t are unique.
