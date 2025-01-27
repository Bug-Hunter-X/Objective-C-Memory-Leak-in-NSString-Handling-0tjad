# Objective-C Memory Leak in NSString Handling

This repository demonstrates a common memory leak in Objective-C related to improper handling of NSString objects within a method. The `bug.m` file showcases the problematic code, while `bugSolution.m` provides the corrected version.

## Problem

The original code creates a new NSString object within a method but fails to release the previously allocated object, leading to memory leaks when the method is called multiple times.

## Solution

The solution involves properly managing the lifecycle of the NSString object. Before assigning a new string, the existing object should be released or set to nil.