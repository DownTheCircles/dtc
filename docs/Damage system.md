# Damage system

The idea of the damage system is rather than having the player giving damage to specific NPCs or objects, every action that might have damage effects, broadcasts damage type and damage amount in a certain area of effect. Objects that can be affected by damage listen for damage being broadcast and if the damage type is something they can react do- they do. 

The idea is that each object will be responsible for it taking damage. 

The advantage of this system is that stuff can be set on fire, enemies will get damaged, brittle stuff will break etc... Another advantage is that objects/NPCs that can react can be later added, without having to change anything of what has already been developed.

![Damage](https://i.ibb.co/vxqZ4pp/damage.png)

This can be used not only for damaging stuff. It can be used by creative players to their advantage. For example setting arrows on fire for a ranged fire damage, if the arrows react to fire. Another example would be water damage to extinguish flames or expose fire enemies.

## Damage types

(To be updated)

| Damage type | Description                                                                                                                                                                                                                                      |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Mechanical  | Basic type of damage. Hitting something would produces this kind of damage. Another way to produce this type for damage is from a falling object. Apart from dealing damage to enemies, it can be used to brake objects, cause avalanches etc... |
| Fire        | Setting things on fire. Certain enemy types can be more susceptible to this type of damage. Certain objects can also be set on fire, eventually destroying them. This can be used for destroying cover for example.                              |
| Water       | Getting things wet. Fire enemies can be weakened by this. Can be used for putting out fires. Can modify internal state of objects- for example making them more resistant to fire damage.                                                        |
| Suffocation | Damage type effective against living things. Also can be used for putting out fires.                                                                                                                                                             |
