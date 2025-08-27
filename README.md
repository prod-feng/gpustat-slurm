# gpustat-slurm

A quick perl script to check GPU nodes information.

Rocky Linux 9.

Slurm, perl, pdsh needed. Need to enable SSH direct login to gpu nodes. pdsh here used to get GPU's temporature.
Now allow "root" user to get the temporature info, needs ssh, so.

## gpustat-cron-job

Most HPC clusters blocks SSH direct login to compute nodes, the alternative way to let all users to run this command is to 
set a cron job as a previleged user to run and produce output to a file, the all other users can run the same command to read from this file.
 


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
