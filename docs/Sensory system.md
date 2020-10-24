# Sensory system

![Sensory system](https://i.ibb.co/tm4Dj1d/sensory.png)

Input from the sensory systems will be used to modify the NPCs default behavior. Basically, every NPC will have its own routine. This routine can be broken up if something is detected. The sensory system will have two components: hearing and vision. Each component will have its own weight. For example hearing would be with less weight, but it will cover more area. 

Vision will have more weight but it's going to be narrower and further reaching. This means that once something is detected in either of the hearing or vision area, an event is being created. This event will have a certain score, based on the components weight and based on what is being detected. So if it is, for example, a very faint noise, it will have a very low weight and based on other factors, like NPC attributes it might get ignored by the NPC. However if it is for example a very loud noise or something like very bright light or seeing the player close to them it will create an event with higher score that has a much smaller chance to get ignored by the NPC.
 So, Once an event is detected by the sensory system, no matter from which component it has come from. It is given a score and a category (danger, point of interest, enemy, etc...). 

So based on this the behavior tree will decide what is going to be the next action of the NPC. 
This way very low scored events have a higher chance of getting ignored, some mid- range events might spark the interest of the NPC and it might go and investigate and if it has a really high value the NPC will engage: attack, start conversation or something else based on the NPCs routines.
