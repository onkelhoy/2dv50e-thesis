
The problem is discribed quite clearly however a better effort can be made to stay more consistant, what I am reffering to is, early on in the thesis their goal is mentioned to be: 

> *"The goal of this project was to conduct a comparative analysis of **Java Virtual and Platform threads** in terms of runtime performance using different thread-safe test cases."* 

But this slightly changes in the related work section to:

> *"To summarize, none of the related work worked directly with **thread factories or executor services** to measure the runtime performance of different thread-safe workloads which opens the possibility for this study to make some contribution in this research area of multi-threading in Java."* 

These two different snippets, even if they might mean the same are slightly different and can impose confusion to readers who does not understand the difference. 

The last sentence feels like a motivation text but it is inside the related work as a summery point to make a stance to all related works, this should not be the case. The motivation part dwells into both scientific reasoning and also industry with a clear motivation that this thesis provides underlaying information to what and how virtual threads works and which one should be choosen between virtual and platform threads. 

The related work seems a little bit off in that theres no clear stance between their work and this study. There is a summery to all related works as mentioned earlier but its general and should be more specific to each case. The second related work should be improved as they seem to claim that its result is not valid because its hard to test and debug libraries similar to what the related paper is using. Otherwise the related work is related as they all do work related to thread and performance. 

The methodology is well explained and motivated, it shall compare the difference in terms of performance by controlled experiments which are then further analysed to complete its research questions. 

The data presented is a big problem for this thesis, theres is roughly 40 pages of diagrams and tables to represent the full test suite and later a summery report. The study explains how they will use time measures to conduct the reasearch but later uses percentage to show what I believe the difference between virtual and platform threads. A more dedicated metric section should be in place, or rather the current should be extended to include why the use of percentage exists. The vast amount of data shown is not confusing but rather overwhelming. 

The conclusions does a good job to speak from the perspective of results, the whole thesis seems to be leaning towards virtual threads and virtual threads in fact is shown to be the better option they still do discuss how CPU intensive problems might be better in traditional platform threads. 

The two objectives of this study has been discussed individually and with the result of the thesis the objectives are met. 

Overall the theis does a good job keeping a good structure but theres a bit of repeated concepts here and there. Examples of those:
- how test will save the time for analysis 
- the setup of tests to use different techniques is illustrated multiple time in both text and code

The thesis mentioned in its motivation that they want to bring knowledge about virtual threads and how it works but they also include big chunk of code to show how java uses a if-statement to either go for virtual thread and platform threads, something that does not really add any value - text can exist to give this background knowledge but code is not necessary. Also for a analysis point of view for the both I dont know what value knowing how java actually does use the both adds much of value in general. 

The amount of code and results should really be re-considered. Both can be added in a github repo and referenced, unique code can be explained with psudocode but implementing merge sort for example does not seem to add much of value here. 

As final words, I don't comment much on positive aspect as I belive they dont give much but to not leave the authers without any cookies: The thesis is good, I really like they made the effort to test multiple different tasks on different OS systems which also has been run multiple times for each of the threading technique. This is very useful information, with a slight fine tuning and reducing the amount of code and results this thesis can be a good demonstaion for its main purpose! The future work section mentions a very valid point, how RAM and CPU can be documented as well, reading files can in-fact put files into the RAM so next time they are read it can speed up and thus result in different results - just a speculation from my side. 