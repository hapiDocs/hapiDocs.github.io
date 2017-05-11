## Overview
The HAPI platform features an in-process scheduler for running periodic jobs. Jobs can be control functions, such as turning a light or pump on. Jobs can also serve monitoring purposes, such as gathering sensor data. Job information is stored in the database, in the table `interval_jobs`. Any Smart Module can run the job scheduling code (i.e. "become the Scheduler"). Dumb modules cannot run become the Scheduler.

## Technical Description
When a HAPI Smart Module starts, it drops on message on the network asking for the Scheduler to respond. If another module on the network is running the job scheduling code, it responds to the to the message and no further action is taken. If there is no response to the message, the starting module runs the job scheduling code itself and announces that it is now the Scheduler. 

## Further Information
The HAPI Scheduler uses [the schedule package](https://pypi.python.org/pypi/schedule) created by Daniel Badr. Documentation can be [found here](https://schedule.readthedocs.io/en/stable/).