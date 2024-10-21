# High Quality, High Performance Screen-Space Ambient Occlusion for OpenMW

This is an attempt to create the best and fastest SSAO shader for OpenMW out there.

![A scene with only SSAO applied](https://i.imgur.com/KvtVvzj.png)

<details>
    <summary>More screenshots</summary>
    <p>SSAO enabled</p>
    <img src="https://i.imgur.com/93YEP5n.png" alt="SSAO enabled">
    <p>SSAO disabled</p>
    <img src="https://i.imgur.com/AbAsgZP.png" alt="SSAO disabled">
</details>

## Features

- **Supports normal maps**: Unlike most SSAO shaders, this shader takes the surface normal into account and so
interacts properly with normal maps and other sub-polygon surface lighting techniques.

- **Temporal reprojection**: SSAO data is shared with past frames, radically improving the quality of occlusion with
improving performance. Unlike other implementations of temporal reprojection, stale data is properly rejected using a
novel frame marking technique to avoid visual issues.

- **Highly configurable**: Find your personal sweet-spoot between quality and performance while achieving the look and
feel you're after.

- **Downsampling & blurring support**: Reduce the performance hit with minimal impact on visual quality.

- **Behaves correctly with complex scenes**: No 'occlusion halo' artifacts, or ghost shadows.

- **Crisp, sharp SSAO**: No 'bleeding' of SSAO in screen-space on to nearby vertices, blending is depth-aware.

- **Minimal flickering or shimmering**: Unlike many other SSAO shaders, this shader exhibits very little flickering,
shimmering, or noise - even when the camera is moving quickly through complex scenes.

- **Handles fog and water properly**: No 'phantom' occlusion for objects hidden behind fog or under the water.

- **Option to disable SSAO for hands**

## Installing

*Ensure that you have the [latest development build](https://openmw.org/downloads/) of OpenMW. If you find that the mod
does not work with the latest development build, please open an issue!*

1. [Download the shaders](https://github.com/zesterer/openmw-ssao/archive/refs/heads/main.zip).

2. Extract the shaders somewhere. I'd strongly suggest extracting next to your `openmw.cfg` file.

3. Add a `data` entry to your `openmw.cfg`, as with most asset mods:

```
data = "path/to/openmw-ssao"
```

(Ensure that the `openmw-ssao` directory contains the `shaders` and `textures` directories)

4. Enable [post-processing shaders](https://openmw.readthedocs.io/en/latest/reference/modding/settings/postprocessing.html#enabled) in your `settings.cfg`.

5. Start OpenMW and have fun!

## Enabling the mod

1. Open the in-game 'Options' menu and enable 'Post Processing' in the 'Video' tab.

2. Press F2 to open the in-game post-processing menu

3. Click on 'ssao'

4. Press shift + right arrow key to add it to the active effects list
