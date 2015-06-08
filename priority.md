# Slurm job scheduling

*What are the criteria used to determine job scheduling?*

Job scheduling is based on priority as determined by slurm's [multifactor plugin](http://slurm.schedmd.com/priority_multifactor.html), which takes into account the amount of time the job has been waiting in the queue, the amount of resources the user has been using recently, and the size of the job (number of nodes).  Note that a user who is currently hogging resources will have their priority reduced when attepting to submit additional jobs.

In general, jobs run based upon priority, but if there aren't enough resources
you won't be able to start your job. If processes on the login nodes are too
disruptive, RCC System Administrators may be forced to terminate them. 

More info on ...

* [priority calculation](https://rcc.uchicago.edu/docs/tutorials/rcc-tips-and-tricks.html#priority)

* [queue limits](https://rcc.uchicago.edu/docs/faq/index.html#what-are-the-queue-limits)
