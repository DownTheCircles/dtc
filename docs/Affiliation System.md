# Affiliation System

![Affiliation system](https://i.ibb.co/1fWj1sk/Affiliation-System.png)

Player connection can range from very negative (-5) to very positive (+5). Your interactions with the AT will modify this value, based on what you do.

Than based on this value, the NPCs own connection and the NPCs attributes its behavior towards you will be decided. Non-AT NPCs will be generated randomly, based on some statistical distribution and also based on this it will be randomly chose to what AT does the NPC has affiliation to.

### Example interactions:

* AT: NPC, that you killed

* Your affiliation value: -5

* NPC: Friend of the AT with positive affiliation

Because the NPC has positive affiliation with the AT and you have strongly negative one, there is a high probability, you'll get attacked.

The same is true with you having strongly positive affiliation and a NPC with negative one.

If your affiliations match, you might get some help- help in combat, be more willing to give you something, help with some knowledge etc.

However, non-ultimate values make for more interesting situation:

* AT: NPC, that was robbed by you

* Your affiliaton value: -2

* NPC: Friend of AT with positive affiliation

Apart from affiliation, the random generation algorithm will be generating other specs of the NPC. For example, the algorithm will be generating values, describing the NPC's personality and attributes for example: strength, charisma, intelligence and other D&D like stuff. Based on this and based on the affiliation value, the NPCs behavior tree will decide the NPCs action towards you. For example if the character strength is lower than the player, based on the low negative value, it won't help you but it will also not attack you. However, if the NPC has low intelligence, it might not be able to understand that it will get beaten up and attack you. This way different types of NPCs will react differently, creating the feel of dynamic and real world, where each NPC is unique and makes its own decisions.

### Default choices

Some NPCs will have default behavior towards you. For example humans will be rather neutral towards you. If you have no connection to their AT- they will not attack you, but also will probably ignore you. 

Daemons, on the other hand, will be aggressive towards you by default. Getting into negative connection with their AT- might mean that they will be more persistent when fighting you and if they have a higher intelligence attribute, might even try to hunt you down. However, getting into a positive connection with their AT might also have some interesting effects. Having weak positive connection, might mean that the daemon NPC will be more reluctant in attacking you. Having a strongly positive connection with their AT- might even mean that the NPC will help you in battle. An idea might be to be able to get a pet, out of a low intelligence daemons by getting a +5 connection with their AT.
