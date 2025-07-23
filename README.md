# rms

It's a simple simulator for the Rate Monotonic scheduling algorithm on a single-core CPU.

## Specification

- The simulator will read a set of periodic tasks from a file and report if the task set is schedulable under Rate Monotonic.
- Also output the number of times each task is preempted in the first hyperperiod.
- The main execution will be in the `ece 652 final.py` file with a single command line argument: the name of the input file containing the tasks to be run. For example:

```bash
python3 ece_652_final.py workload1.txt
```

- The input file will contain a set of tasks, each defined by one line.
- Each task line will contain three positive numbers (not necessarily integers - precision up to 0.001) separated by commas.
- The line format is:

```
<execution time>,<period>,<deadline>
```

- The output will be printed to the standard output with two lines:
    - The first line will be `0` or `1` indicating whether the task set is schedulable under Rate Monotonic (`0` for not schedulable, `1` for schedulable).
    - Only when the first line is `1`, the second line should be the number of times each task is preempted in the first hyperperiod. These preemption counts should be in-order of task and separated
      by a comma.
- Do not use Python features newer than version 3.10.
- Do not import any libraries that are not included in a default installation of Python 3.10 (except that you may optionally import numpy).
- Your program will be given a maximum of 60 seconds of execution time for each task set
