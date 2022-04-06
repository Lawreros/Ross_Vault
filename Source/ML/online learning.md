name : online learning
tags : 
backlinks : 
source : #HOML 

###### Content:
In online learning, you train the system incrementally by feeding it data instances sequentially, either individually or by small groups called mini-batches. Online learning is great for systems that receive data as a continuous flow and need to adapt to change rapidly or autonomously.
![[Pasted image 20210706175652.png]]

Online learning algorithms can also be used to train systems on huge datasets that cannot fit in one machine's main memory (this is called *out-of-core learning*). The algorithm loads part of the data, runs a training step on that data, and repeats the process until it has run on all of the data.

###### Properties:
- One important parameter of online learning system is how fast they should adapt to changing data: this is called the [[learning rate]].
- A big challenge with online learning is that if bad data is fed to the system, the system's performance will gradually decline.

###### Additional Thoughts:
