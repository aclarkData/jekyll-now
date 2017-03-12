---
published: true
---
## Scheduling a python program using windows Task Scheduler

When I began programming and tried to schedule some analytic jobs on my work machine, I had a hard time figuring out how to get the windows task scheduler to work with python. Usually, with stack overflow and the like, it is very easy to find resources to answer this sort of question, but I had a hard time finding anything that explained how to schedule a python job. This post is an attempt to remedy this situation.

* Find where python lives on your machine to fill the 'program' slot in the scheduler.
![Step 0](/images/version location.PNG)
* Go to the Task Scheduler and select 'Create Task'

![Step 1](/images/sch0.PNG)

* Type in the name of the task, a description, if desired.

![Step 2](/images/sch1.PNG)

* Then, go to the 'Triggers' tab and select time interval, One Time, Daily, Weekly or Monthly, and specify a start time, etc. Make sure the checkbox at the bottom is checked 'Enabled'.

![Step 3](/images/sch2.PNG)
* Go to the 'Actions' tab, the hardest to get right, so take note, and put the path determined earlier to your python exe, into the 'Program/script' line. Add the name of your .py file in the 'Add arguments' line, and finally, add the starting directory, such as: C:/Users/aclark/desktop in the 'Start in' line.

![Step 4](/images/sch3.PNG)

* I've never messed with these settings though, so do at your own risk.
![Step 5](/images/sch35.PNG)

* Finally specify when a job would get killed, etc and push 'OK', you are good to go!
![Step 6](/images/sch4.PNG)
