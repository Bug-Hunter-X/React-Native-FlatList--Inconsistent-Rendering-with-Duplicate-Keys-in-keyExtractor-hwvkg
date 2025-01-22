# React Native FlatList: Inconsistent Rendering with Duplicate Keys

This repository demonstrates a common error in React Native's FlatList component: inconsistent rendering caused by a `keyExtractor` function that doesn't provide unique keys for each item.  The `bug.js` file shows the problematic code, and `bugSolution.js` provides the corrected version.

## Problem

When the `keyExtractor` function in `FlatList` returns duplicate keys, React Native can't reliably track and update items.  This results in inconsistencies like missing or duplicated items in the list, especially when data changes.

## Solution

The solution is to ensure that the `keyExtractor` always generates unique keys for each item in the data array.  This often involves using a unique identifier from the data itself, or generating a UUID if no suitable identifier exists.