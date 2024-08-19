# Halo 3 Tag Fixes
This repository contains several tags for use with the H3EK, these tags fix several oversights made during Halo 3's development and other quality of life improvements.

# Installation
These tags are meant to overwrite the existing tags in your H3EK tags directory, if you modified them before make sure to back those up before installing!

Simply just download the repository and drag and drop the "tags" folder from the repository into your H3EK folder. When asked to replace, hit "Yes".


# Fixes
Currently, the following tags have been modified:

### objects\weapons\grenade\frag_grenade\frag_grenade.projectile
In the attachments block the `projectile.light` tag now parents to the `light` marker instead of the invalid `root` marker, which allows the light to appear again when throwing the frag grenade