# Lua Pairs Iterator Bug

This repository demonstrates a potential issue with Lua's `pairs` iterator when dealing with tables that are modified during iteration. The `bug.lua` file contains code that exhibits this problem.  The solution is provided in `bugSolution.lua`.

**Problem:** The original code recursively iterates through a nested table. However, if the table structure is modified during iteration, `pairs` might skip elements or enter an infinite loop.  This can be particularly subtle and difficult to debug.

**Solution:** The solution demonstrates a safer approach, copying the table keys before iterating to prevent issues caused by modifications during the iteration process.