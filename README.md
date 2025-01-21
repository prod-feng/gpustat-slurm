# gpustat-slurm

A quick perl script to check GPU nodes information.

Rocky Linux 9.

Slurm, perl, pdsh needed. Need to enable SSH direct login to gpu nodes.

The output of this script is as following:

```

$ gpustat
     NODE     LOAD    CPUS    MEMORY(GB)   STATE     GRES             Hi-Temporature
...
   node002  15.02    15/16    45/ 69/ 95    mix   9/gpu:4000:8,gpu:6000:2    81
...
   node012   0.01     0/48    50/765/772   idle   0/gpu:a4000:8              26
...
   node018   0.00     0/40    50/ 92/ 95   idle   0/gpu:4000:4               30
CPUS lists allocated/total CPU cores. 
MEMORY(GB) lists allocated/free/total memory in GB. 
GRES lists allocated/total GPUs. 

```
