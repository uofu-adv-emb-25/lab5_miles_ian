## Approach to Calculations
Jitter was calculated as the deviation of the measured signal's period from the ideal period.

Drift was calculated by projecting the difference in signal periods over the span of an hour:
We first calculated the difference between ideal periods/hr and measured periods/hr, then we translated these differences to percentages representing how much faster or slower our measured signal was compared to the ideal.

Our ideal period was set to be 20ms across all experiments.
For activity 1, we used a no-op for loop with 2 million iterations to introduce differences in signal outputs.
For activity 2, we used a no-op for loop with 200 thousand iterations to introduce differences in signal output.

We used our oscilloscope's measured statistics and outputted these as .csv files to gather/process data. It appears that some very small non-zero values were rounded or truncated to zero - these are indicated by "~0". 

## Results
### task_delay w/o Busy Loop
Jitter: ~0 ms
Drift: 0.0017% slower

### task_delay w/ Busy Loop
Jitter: 128.0004 ms
Drift: 86.5% slower


### sleep w/o Busy Loop
Jitter: ~0 ms
Drift: 0.0017% slower

### sleep w/ Busy Loop
Jitter: 128.0004 ms
Drift: 86.5% slower


### timer w/o Busy Loop
Jitter: ~0 ms
Drift: 0.0017% slower

### timer w/ Busy Loop
Jitter: 332.0104 ms
Drift: 94.32% slower



### gpio_interrupt w/o Busy Loop
The delay between the sync signal and the board output was negligable (~0 ms)

### gpio_interrupt w/ Busy Loop
Delay: 8 ms

