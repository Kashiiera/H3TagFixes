# Halo 3 Tag Fixes
This repository contains several tags for use with the H3EK, these tags fix several oversights made during Halo 3's development and other quality of life improvements.

# Installation
These tags are meant to overwrite the existing tags in your H3EK tags directory, if you modified them before make sure to back those up before installing!

Simply just download the repository and drag and drop the "tags" folder from the repository into your H3EK folder. When asked to replace, hit "Yes".


# What has changed?
Currently, the following fixes and QoL improvements have been implemented:

## Cubemaps
> [!NOTE]
> 
> Regenerating cubemaps on "The Covenant" results in a crash meaning this repository does not include them.
>

> [!NOTE]
> 
> Only cubemaps placed in the scenario themselves have been regenrated, standalone cubemaps referenced in shaders have not been regenerated.
> 

All scenario cubemaps have been regenerated with compression disabled, removing visual artifacts and washed out colors

Before:
![Cubemaps on Icebox before regenerating cubemaps with compression disabled](assets/cubemaps_turf_before.png)
After:
![Cubemaps on Icebox after regenerating cubemaps with compression disabled](assets/cubemaps_turf_after.png)

## Arbiter
Arbiter in Campaign Co-Op now has sounds for dying and being damaged heavily again, previously the dialogue field was empty which meant he had no dialogue at all. This field is now pointing to a new `arbiter_coop.dialogue` tag which only consists of `dth`, `pain` and `thrwn` sound tags.

## Elites
Elites in Campaign Co-Op and Multiplayer now play their correct shield low, shield depleted and shield recharging sounds instead of playing Masterchief's. This also applies to Co-Op Arbiter.

## Frag Grenades
Frag Grenades now emit a light again when thrown like in previous games

The light was parented to an invalid marker which meant the light would just not create at all, parenting the light to the `light` marker allows it to attach again