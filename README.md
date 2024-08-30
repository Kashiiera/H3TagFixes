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


## Frag Grenades

### objects\weapons\grenade\frag_grenade\frag_grenade.projectile
In the attachments block the `projectile.light` tag now parents to the `light` marker instead of the invalid `root` marker, which allows the light to appear again when throwing the frag grenade

[def]: https://myoctocat.com/assets/images/a-octocat.svg