# Halo 3 Tag Fixes
This repository contains several tags for use with the H3EK, these tags fix several oversights made during Halo 3's development and other quality of life improvements.

# Installation
These tags are meant to overwrite the existing tags in your H3EK tags directory, if you modified them before make sure to back those up before installing!

Simply just download the repository and drag and drop the "tags" and "data" folder from the repository into your H3EK folder. When asked to replace, hit "Yes".

# What has changed?
Currently, the following fixes and QoL improvements have been implemented:

## Cubemaps
> [!NOTE]
> 
> Regenerating cubemaps on "The Covenant" results in a crash meaning this repository does not include them.
>

> [!NOTE]
> 
> Only cubemaps placed in the scenario themselves have been regenrated, cubemaps generated with "screenshot_cubemap" have not been regenerated.
> 

All scenario cubemaps have been regenerated with compression disabled, removing visual artifacts and washed out colors

Before:
![Cubemaps on Icebox before regenerating cubemaps with compression disabled](assets/cubemaps_turf_before.png)
After:
![Cubemaps on Icebox after regenerating cubemaps with compression disabled](assets/cubemaps_turf_after.png)

## Arbiter
Arbiter in Campaign Co-Op now has sounds for dying and being damaged heavily again, previously the dialogue field was empty which meant he had no dialogue at all. This field is now pointing to a new `arbiter_coop.dialogue` tag which only consists of `dth`, `pain` and `thrwn` sound tags.

## Elites
> [!NOTE]
> 
> All of these fixes and changes will also apply to both Arbiter and Co-Op Arbiter
>

Elites in Campaign Co-Op and Multiplayer now play their correct shield low, shield depleted and shield recharging sounds instead of playing Masterchief's.

Elites will now keep their rifles lowered when walking around while weapons are lowered, previously they were only lowered if they were standing still.

## Flood Combat Forms
Fixes collision issues with all Flood Combat Forms. 

By default the collision for limbs and corpses remained and did not contribute to the damage taken by Flood Combat Forms and for the Elite Flood Combat Forms in specific, the "Destroyed Torso" permutation was incorrectly labelled as "Destroyed Head" which meant that hitting a headless Elite Flood Combat Form at specific spots did not deal any damage.

## Frag Grenades
Frag Grenades now emit a light again when thrown like in previous games

The light was parented to an invalid marker which meant the light would just not create at all, parenting the light to the `light` marker allows it to attach again

# Credits

### Kashiiera
* Restoring Arbiter's Co-Op dialogue
* Restoring the CHUD sounds for Elites
* Restoring missing lights for Frag Grenades

* Fixing Elites their rifles not staying lowered while walking around

### theHostileNegotiator
* Fixing the collision models for the Flood Combat Forms

### J-S
* Figuring out the solution to very compressed cubemaps