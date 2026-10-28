# Oliver's Game Engine
This game engine was built from a series of YouTube tutorials on how to build a game engine with Swift and Metal, although greatly expanded.

The original YouTube series is here: https://www.youtube.com/playlist?list=PLEXt1-oJUa4BVgjZt9tK2MhV_DW7PVDsg

The published code going along with that YouTube series is here: https://github.com/twohyjr/Metal-Game-Engine-Tutorial/

## Features
The Engine supports:
- Skeletal Animation
- Frustum Culling
- Blinn-Phong shading (expanded from Phong shading in the original)
- Reflections
- Shadows
- Transparency

## Basic Architecture
The Renderer is the core of the application. The render flow looks something like this:
- Call Update on the SceneManager, which updates deltaTime and provides that to all children and any associated animations
- Render shadows
- Render reflections
- Render everything else using the shadow and reflection maps generated in the previous two steps
- Repeat
To render the scene, it calls SceneManager.setupRender. All objects add themselves to the array stuffToRender in RenderVariables. The Renderer then proceeds with draw calls for each object.

## Asset Credits:
prinmath.com
kenny.nl
Quaternius
The Blender Foundation
