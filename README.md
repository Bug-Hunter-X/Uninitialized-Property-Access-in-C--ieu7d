# Uninitialized Property Access in C#

This repository demonstrates a common, yet easily overlooked, error in C#: accessing a property before it has been explicitly assigned a value.  Uninitialized properties have default values (e.g., 0 for integers, null for reference types), but relying on these defaults can introduce subtle bugs and make your code harder to maintain.

## The Problem

The `bug.cs` file shows a simple class with a property `MyProperty`. The `MyMethod` attempts to access and print `MyProperty` before a value has been assigned.  While it *might* print 0, this is not guaranteed and can lead to unexpected behavior depending on the class's lifecycle and other factors.

## The Solution

The `bugSolution.cs` file provides a corrected version.  It explicitly initializes `MyProperty` before accessing it in `MyMethod`.  This ensures predictable behavior and prevents potential errors.