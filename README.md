#### task_delay w/o Busy Loop
Jitter (from std dev) = ~0 ms
Drift: 0.0017% slower

#### task_delay w/ Busy Loop
Jitter = 148.0004 ms - 20 ms = 128.0004 ms
Drift: 86.5% slower

#### Sleep w/o Busy Loop
Jitter (from std dev) = ~0 ms
Drift: 0.0017% slower

#### Sleep w/ Busy Loop
Jitter = 148.0004 ms - 20 ms = 128.0004 ms
Drift: 86.5% slower

#### Timer w/o Busy Loop
Jitter (from std dev) = ~0 ms
Drift: 0.0017% slower

#### Timer w/ Busy Loop
Jitter = 352.0104 ms - 20 ms = 332.0104 ms
Drift = 94.32% slower

#### gpio_interrupt delay w/o Busy Loop
The delay between the sync signal and the board output was negligable (~0 ms)

#### gpio_interrupt delay w/ Busy Loop
Delay = 8 ms

