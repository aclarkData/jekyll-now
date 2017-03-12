---
published: false
---
## Scheduling a python program using windows Task Scheduler

When I began programming and tried to schedule some analytic jobs on my work machine, I had a hard time figuring out how to get the windows task scheduler to work with python. Usually, with stack overflow and the like, it is very easy to find resources to answer this sort of question, but I had a hard time finding anything that explained how to schedule a python job. This post is an attempt to remedy this situation.

1. Find where python lives on your machine to fill the 'program' slot in the scheduler.
![Step 0](/images/version location.PNG)

2. Go to the Task Scheduler and select 'Create Task'
![Step 1](/images/sch0.PNG)

![Step 2](/images/sch1.PNG)

![Step 3](/images/sch2.PNG)

![Step 4](/images/sch3.PNG)

![Step 5](/images/sch35.PNG)

![Step 6](/images/sch4.PNG)
