---
title: "Submitting"
weight: 10
---

### Creating a PBS Script

To set the parameters for your job, you can create a control file that contains the commands to be executed.

Typically, this is in the form of a PBS script. This script is then submitted to PBS using the `qsub` command.

Here is a sample PBS file for **running wrf.exe**, named **myjobs.pbs**, followed by an explanation of each line of the file.

```
#!/bin/bash
#PBS -N <job_name>
#PBS -q <queue_name>      # low,high,Addnode,zhao
#PBS -l nodes=<N>:ppn=<M> # Number of nodes, number of processors each node
cd $PBS_O_WORKDIR     # change to the directory from which the job was submitted
nprocs=`cat $PBS_NODEFILE | wc -l` # Get number of processors allocated
mpirun -np $nprocs ./wrf.exe  # run the command
```

- The first line in the file identifies which shell will be used for the job.  In this example, bash is used;

- The second line specifies the name of queue. Please check [node allocation](https://hpc-nuist-ap.github.io/overview/node-allocation/) chapter;

- The third line specifies **the number of nodes and processors each node** desired for this job. In this example, one node with two processors is being requested;

- The fourth line tells the HPC cluster to access the directory where the data is located for this job. In this example, the cluster is instructed to change the directory to where the job was submitted. Absolute path also works;

- The fifth line calculates number of processors allocated;

- The sixth line tells the cluster to run the program. In this example, it runs wrf.exe using N\*M processors.

### Using the qsub Command

To submit your job without requesting additional resources, issue the command

```
$ qsub myjob.pbs
```

#### Matlab Script

```
#!/bin/bash
#PBS -N job_name
#PBS -q queue_name
#PBS -l nodes=N:ppn=M
cd $PBS_O_WORKDIR
matlab -nodisplay < <matlab_script_name>
```

#### Python Script

```
#!/bin/bash
#PBS -N job_name
#PBS -q queue_name
#PBS -l nodes=N:ppn=M
cd $PBS_O_WORKDIR
export PATH=/public/software/anaconda/anaconda3/bin:$PATH
. /public/software/anaconda/anaconda3/etc/profile.d/conda.sh
conda activate python36
python <python_script_name>
```

#### References

1. [Running a Job on HPC using PBS](https://hpcc.usc.edu/support/documentation/running-a-job-on-the-hpcc-cluster-using-pbs/)