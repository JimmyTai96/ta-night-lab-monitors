# ta-night-lab-monitors

A Java multithreading simulation of students visiting a TA's night lab hours, using **monitors** (`synchronized`, `wait`, `notify`).

## The problem

The TA can help at most **3 students at a time**, and 20 student threads arrive at once. Students over the limit must wait until a spot frees up.

| Class | Role |
| --- | --- |
| `TA_Brain` | The monitor: tracks capacity, makes students `wait()` when full, `notify()`s when a spot opens |
| `Student` | Thread that asks the TA for help |
| `TA` | Thread that gives advice and releases students |
| `NightLab` | Driver: creates the monitor and starts all threads |

## Run

```bash
javac *.java
java NightLab
```

```
studentNum0 is with the TA.
studentNum2 is with the TA.
studentNum1 is with the TA.
studentNum3 is Waiting for a spot with TA.
...
```

Concurrency coursework.
