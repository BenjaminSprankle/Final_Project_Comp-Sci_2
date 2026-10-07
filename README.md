# Priority-Based Weekly Scheduler

A C++ console application that schedules tasks into a seven-day week by priority, subtracts blocked time, and reports work that cannot fit.

**Author:** Ben Sprankle  
**Context:** Chaffey College final project, April 2025  
**Testers credited in source:** Ben Sprankle, Martin Aguilar, Jacob Huerta

## What it does

- Collects task names, unique priorities, and estimated durations.
- Sorts tasks by priority using bubble sort.
- Starts each day with 16 available hours.
- Subtracts user-entered blocked time from each day.
- Splits tasks across days when needed.
- Reports any remaining unscheduled hours.

The project uses a `BaseScheduler` interface and a `Scheduler` implementation to demonstrate inheritance and polymorphism.

## Compile and run

The tracked source is named `Project.C++`. Explicitly selecting C++ makes the command work regardless of how the compiler interprets that extension.

```bash
g++ -std=c++11 -x c++ Project.C++ -o scheduler
./scheduler
```

On Windows, run `.\scheduler.exe` after compilation.

## Example

For a task named `Homework` with an estimate of 20 hours, no blocked time, and highest priority, the scheduler allocates 16 hours on Day 1 and 4 hours on Day 2.

## Scope and known limitations

This is an educational command-line project. Task names are read as single words. Numeric input stream failures are not recovered, and repeated blocked-time entries can exceed a day's capacity. The task-duration check currently allows up to 156 hours even though its prompt says 16.

[Final report](Final_Report.md) preserves the original project writeup.
