# Slurm

* [docs](https://computing.llnl.gov/linux/slurm/)
* [quickstart](https://computing.llnl.gov/linux/slurm/quickstart.html)
* [tutorials](http://schedmd.com/slurmdocs/tutorials.html)


## Overview

Slurm is a cluster workload manager. It has three key functions: resource
allocation, arbitration, and management.

* It allocates exclusive and/or non-exclusive access to resources (compute nodes) to users for some duration of time so they can perform work. 

* It arbitrates contention for resources by managing a queue of pending work.

* It provides a framework for starting, executing, and monitoring work (normally a parallel job) on the set of allocated nodes. 


## Commands

See the [quick start](https://computing.llnl.gov/linux/slurm/quickstart.html)
user guide for an overview.

* `squeue` - report state of jobs or job steps
* `sinfo` - report state of nodes and partitions
* `smap` - similar to `sinfo` but uses graphical display to reflect topology
* `sstat` - get status of currently running jobs

Both `sinfo` and `squeue` have a wide variety of filtering, sorting, and formatting options. 

There are a few tools available to work with accounting data: `sacct`, `sacctmgr`, and `sreport`. These tools all get or set data through the **SlurmDBD** daemon.

* `sacct` - get job accounting info about active or completed jobs
* `sacctmgr` - add or remove clusters, add or remove users, etc.
* `sreport` - generate various reports on usage collected over a given time period

The `sacct` command can report resource usage for running or terminated jobs including individual tasks, which can be useful to detect load imbalance between the tasks. The `sstat` command can be used to status only currently running jobs. It also can give you valuable information about imbalance between tasks. The `sreport` command can be used to generate reports based upon all jobs executed in a particular time interval.


## Quick tips

List all slurm accounts:

    sacctmgr list account

List top `N` users:

    sreport user top topcount=N

Example usage of `sacct`

    sacct --starttime=060114 --endtime=070114 --accounts=pi-depablo --allusers

    sacct -P
      --starttime 07/01/12 
      --account=rcc-staff 
      --allusers 
      --allocations 
      --format=Account,CPUTimeRAW,Eligible,End,JobName,JobID,
               NCPUS,NNodes,Partition,QOS,Start,State,Submit,Timelimit,User

This generates the following output:

    Account|CPUTimeRAW|Eligible|End|JobName|JobID
      |NCPUS|NNodes|Partition|QOS|Start|State
      |Submit|Timelimit|User

    rcc-staff|606|2014-07-01T09:08:09|2014-07-01T09:18:16|_interactive|8997232
      |1|1|sandyb|sandyb|2014-07-01T09:08:10|CANCELLED by 891783663
      |2014-07-01T09:08:09|02:00:00|wettstein

    rcc-staff|17|2014-07-01T09:35:03|2014-07-01T09:35:21|_interactive|8997363
      |1|1|sandyb|sandyb|2014-07-01T09:35:04|COMPLETED
      |2014-07-01T09:35:03|02:00:00|robinweiss

Note that we have a bash wrapper for `sacct` that provides some helpful additional parsing.  Use the `--help` and `--usage` flags for details.

    sacct-plus --user all --start "last week" -P --format "jobname,jobid,state"

Example usage of `sacctmgr`:

    sacctmgr list qos

    sacctmgr list qos format=Name,MaxNodes

    sacctmgr -P list qos format=Name
