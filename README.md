# IntelliLight



This project has been published as the following conference paper:

> Hua Wei\*, Guanjie Zheng\*, Huaxiu Yao, Zhenhui Li, IntelliLight: A Reinforcement Learning Approach for Intelligent Traffic Light Control, in Proceedings of the 2018 ACM SIGKDD International Conference on Knowledge Discovery and Data Mining (KDD'18), London, UK, August 2018. 
>
> (\*Co-First author.)



The full paper and demo can be found at the author's website.



This project proposes a reinforcement learning based intelligent traffic light control system. Simply run the runexp.py to run the experiment. Please change the parameters in conf/ folder and runexp.py correspondingly if needed. Also, please specify the location of TraCI module in map_computor.py if necessary.




Before running above codes, you may need to install following packages or environments:

- Python 3.6
- SUMO 0.32 with TraCI module. Please specify TraCI location correpsondingly in map_computor.py
- Keras 2.2.0 and Tensorflow 1.9.0





The files are functioning like this:

- runexp.py

  Load the experiment setting, and call traffic_light_agent.

- traffic_light_dqn.py

  Simulate the reinforcement learning agent. This file simulates the timeline, get current state from sumo_agent, get current state from sumo_agent and call the agent to make decision.

- sumo_agent.py

  Interact with map_computor to get state, reward from the map_computor, and convey action to map_computor.

- map_computor.py

  Read data from SUMO and operate SUMO.

- agent.py

  Abstract class of agent.

- network_agent.py

  Abstract class of neural network based agent.

- deeplight_agent.py

  Class of our method.

- conf/

  Configuration files.

- data/

  Traffic flow files. The intersection is connected with four road segments of 300-meters long.		


  ​


If you are new to SUMO, hope these slides can help you with a good start (http://personal.psu.edu/hzw77/posts.html#sumo-introduction).



**Citation**

```
@inproceedings{Wei:2018:IRL:3219819.3220096,
 author = {Wei, Hua and Zheng, Guanjie and Yao, Huaxiu and Li, Zhenhui},
 title = {IntelliLight: A Reinforcement Learning Approach for Intelligent Traffic Light Control},
 booktitle = {Proceedings of the 24th ACM SIGKDD International Conference on Knowledge Discovery \&\#38; Data Mining},
 series = {KDD '18},
 year = {2018},
 location = {London, United Kingdom},
 pages = {2496--2505},
 numpages = {10},
 publisher = {ACM},
 address = {New York, NY, USA},
}
```
