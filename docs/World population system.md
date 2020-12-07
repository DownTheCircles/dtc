# World population system

<img src="https://i.ibb.co/H2wd0Tm/wprld-population.png" title="" alt="World Population" width="821">

## World behavior tree layer system

![Behavior tree layers](https://i.ibb.co/XDj5Vvy/Behavior-Tree-Layers-System.png)

The idea is that there are going to be different behavior trees at different levels in the game, with each layer, passing the its output to the behavior trees below. This way what can be achieved is the illusion of a world, that exists without the player observing it. This is how it will work:

* A single world behavior tree, that has statistical distribution data for the different NPC types and some data about their behavior. This will be highly abstracted behavior tree, with very simple logic, that lays the foundation for the other, more complex, behaviors. The output of this tree will be a count and type distribution of NPCs between circles- which are the biggest area type in the game (like Forgotten Crossroads, Fungal Wastes etc.. in Hollow Knight), for all circles.

* 9 Circle behavior trees. Only the one, where the player currently is will be active at a time. This way, abstracted behavior will be provided by the world behavior tree for each circle, so there is the feeling that things happen event when the player is not there, but more- specific behaviors will be run only for the circle, where the player is. The output of this tree will be the distribution of NPCs between different areas of the circle for all areas. This tree will be much more complicated than the world tree and will be making decisions based on player influence of the world and overall world state (like time of day for example). Intended result is that NPCs can move between areas during different parts of the day and responding to different world events, simulating a personal routine. The advantages are that actual NPCs will not exist in areas, where the player is not, but will look like they are coming and going from other areas, imitating complex behavior, which would be true, without a player around them.

* Multiple area behavior trees. Each area in a circle will have its simple behavior tree, getting data from the circle behavior tree and distributing NPCs around locations and objects in itself. A simple example- the circle tree might have passed that there should be 30 NPCs, suffering and being tortured. From this the area behavior tree might distribute the NPCs around different torture devices in itself. The output of this tree will be exact spawn location for all NPCs, along with their type and some other behavior parameters.

* A behavior tree for each NPC. This tree will directly control NPC behavior- resulting in animations and interactions. This behavior will be based on some NPC behavior traits, passed by the area tree, the affiliation and sensory system data.

The end result will be that there are going to be just a few active trees, on a few layers- with the complexity and specificity of the tree getting higher with the depth of the layers:

* All current area NPCs behavior trees active- providing highest level of detail behavior

* Current area behavior tree active- providing distribution and base behavior types for all NPCs inside

* Current circle behavior tree active- providing basic routine and NPC movement between areas

* World behavior tree active- providing type and distribution of NPCs between circles

![Multiple trees visualized](https://i.ibb.co/k44fQxf/Behavior-Tree-Layers-System-Page-2.png)
