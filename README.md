<p align="center">
<br/>
  <img src="editor/assets/logo/free_logo_2.png" width="80px"/><br/>
  ΛVΛb<br/>
  Modified version of the AVA engine<br/>
  With some neat stuffs included<br/>
<br/>|
  <a href="#features">Getting Started</a> |
  <a href="#documentation">Documentation</a>|
<br/>
</p>

## Documentation
----

## Roadmap ᕕ(ᐛ)ᕗ

- [x] 00 Project structure, build system and makefiles.
- [x] 01 Window, rendering contexts and game loop.
- [ ] 02 File formats, hashing, encryption and compression.
- [x] 03 Timers, easings and interpolation.
- [ ] 04 Input bindings, digital+analog buttons, filters, gestures, chords and combos.
- [x] 05 Linear math, geometry, volumes and collisions.
- [x] 06 Cameras and frustum culling.
- [ ] 07 Regions, triggers, trees and spatial partioning.
- [ ] 08 Data pipeline and asset journaling.
- [ ] 09 World streaming and level loading.
- [ ] 10 2D/2.5D/3D/VR renderer and post-effects.
- [x] 11 Fonts, atlases and text rendering.
- [x] 12 Debug draw and debug UI.
- [ ] 13 Procedural content, brushes, voxels, noise and CSG.
- [ ] 14 Static meshes, decals, skyboxes and skydomes.
- [ ] 15 Sprites, sheets and spines.
- [ ] 16 Particles, billboards, emitters, trails and paths.
- [ ] 17 Skeletal animation, blending, blendspaces, IKs.
- [ ] 18 LODs, mesh instancing and scenegraphs.
- [ ] 19 Server/client architecture.
- [ ] 20 Message pipeline and serialization.
- [ ] 21 Digital signals, message buffering and event polling.
- [ ] 22 Entity/component/systems and world replication.
- [ ] 23 Scripting, bindings and game modules.
- [ ] 24 Navpoints, navmesh traversal and pathfinding.
- [ ] 25 AI, H/FSM, behavior trees and flocking.
- [ ] 26 Game flow and game UI.
- [ ] 27 Localization, subtitles and unicode.
- [ ] 28 2D/3D audio, HRTF, FFT, filtering and sound occlusion.
- [ ] 29 Dialogue, quests and inventory.
- [ ] 30 Full Motion Video and integrated cinematics.
- [ ] 31 Editor, gizmos, properties, timeline and data tracks.
- [ ] 32 Debugger, callstack, inspection, console, leaks, cvars and profiling.

## Getting started

Execute the `make.sh.bat` script file to build & run the editor.

Additionally:
- `make`                        (launch editor)
- `make game [platform]`        (launch game)
- `make make [game] [platform]` (make game.exe executable)
- `make cook [game] [platform]` (cook all raw game assets)
- `make pack [game] [platform]` (pack all cooked game assets into game.pak file)
- `make fuse [game] [platform]` (fuse game.pak and game.exe both together)

## Disk structure

- `editor/`, generic 3d editor and viewer.
- `engine/`, portable engine runtime.
- `games/`, games and demos.
- `tools/`, build tools & generic asset pipeline.

### AVA as engine:
- [x] Compile the amalgamated `engine.c` source file to get a functional game engine.
- [x] Compile your game as a dynamic library and place it near the `AVA` executable.
- [x] Tip: Rename both executable and dynamic library as desired. Ie, `game.exe` with `game.dll` will work.
- [x] Tip: Place an `.ico` icon close to the binary if you want to as well.
```lisp
cl      engine.c                && echo AVA as engine (Windows)
g++     engine.c                && echo AVA as engine (Linux)
clang++ engine.c                && echo AVA as engine (OSX)
```

### AVAb as library:
- [x] Compile your game and link amalgamated `engine.c` source file with it.
```lisp
cl      game.c engine.c         && echo AVA as library (Windows)
g++     game.c engine.c         && echo AVA as library (Linux)
clang++ game.c engine.c         && echo AVA as library (OSX)
```

### Redistribution
```
- game.exe + .ico        (engine player)
- game.dll/.lua/.socket     (game logic) \
- game.rom/.pak        (ro data storage) | game :)
- game.ram/.sql        (rw data storage) /
```

## License
----
