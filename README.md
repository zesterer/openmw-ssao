# High Quality Screen-Space Ambient Occlusion for OpenMW

## Features

- Normal-aware: Unlike most SSAO shader mods, this shader takes the surface normal into account and so interacts
  properly with normal maps and other sub-polygon surface lighting techniques.

- Temporal filtering: occlusion information is shared between frames, radically improving the quality of occlusion
  without hurting performance.

- Many parameters to configure: Find your personal sweet-spoot between quality and performance while achieving the
  look and feel you're after.

- Downsampling & blurring support: Reduce the performance hit with minimal impact on visual quality.

- Behaves correctly with complex scenes: No more 'occlusion halo' artifacts.

- Handles fog and water elegantly: No 'phantom' occlusion for objects hidden behind fog or under the water.
