name : batch learning, *offline learning*
tags : 
backlinks : 
source : #HOML 

###### Content:
In batch learning, the system is incapable of learning incrementally: it must be trained using all the available data. First the system is trained, and then it is launched into production and runs without learning anymore; it just applies what it has learned.
If you want a batch learning system to know about new data, you need to train a new version of the system from scratch on the full dataset, then stop the old system and replace it with a new one.

###### Properties:
- Training on the full set of data requires a lot of computing resources. If your system needs to be able to learn autonomously and it has limited resources, then you should use [[online learning]] methods.

###### Additional Thoughts:
