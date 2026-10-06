# Minecraft: default-texture block world

## Baseline

Minecraft Java-style default texture vocabulary, simple vanilla Fancy-like lighting, no shaders or Vibrant Visuals by default. “Classic” here means the familiar block-world rendering, not the historical Minecraft Classic release or a byte-identical pre-1.14 texture pack. If a user wants a particular old texture pack, shader or Vibrant Visuals screenshot, use that reference and label the result accordingly.

## Translate the scene

| Source | Rebuild |
| --- | --- |
| Building / pavement | Large cuboid stone, terracotta or stone-brick-like faces on a consistent coarse world grid; doors roughly two blocks tall establish scale |
| Glass | Square pane assemblies with restrained flat pixel streaks, not photographic transparency and reflections |
| Bench / furniture | Plausible wooden stairs, slabs and cuboids; avoid a smooth realistic model with a pixel filter |
| Foliage | Cubic leaf masses, block trunks and flat pixel cutout plants / vines; no thousands of tiny cubes per leaf |
| Person | Player-like cuboid head, rectangular torso, arms and legs; skin-like flat pixel facial and clothing detail; outfit and pose carry source recognizability |
| Curved or absent vanilla prop | Simplified stepped cuboid equivalent retaining its object class and silhouette; explicitly allow this artistic approximation, not a claim of vanilla availability |

Keep crisp low-resolution square texels on each block face, roughly the visual density of default 16×16 block textures. This is an appearance target, not a verified texture resolution. Texture pixels are much smaller than geometry blocks: do not confuse them and build everything from tiny voxels. Use larger planes and a coherent grid rather than an arbitrary voxel miniature.

Lighting should use readable per-face shading, modest corner darkening and block-level local light. In the simple baseline, rain does not turn stone pavement into a mirror. Avoid reflected windows, shiny wet asphalt, volumetric lantern beams, glow spilling over the entire frame, cinematic depth of field or rounded toy bevels.

## Typical failures and narrow repairs

- Looks like pixelated photography: replace remaining photographic faces, foliage and plaster with explicitly described game geometry and flat texels.
- Looks like a shader-pack showcase: remove wet-ground reflections / specular shine, glare and volumetric light; keep flat matte stone and simple local brightness.
- Looks like LEGO or a voxel diorama: remove stud shapes / bevels and tiny cubes, increase architectural block size, retain eye-level source perspective.
- Character becomes a tiny mascot: use Minecraft player proportions and retain its original full-body screen position. Block conversion still changes fine identity.

## Sources

The [Minecraft texture artist interview](https://www.minecraft.net/en-us/article/try-new-minecraft-textures) discusses block texture scale and avoiding overly detailed voxel models. The [official Vibrant Visuals page](https://www.minecraft.net/en-us/vibrant-visuals-update) describes enhanced lighting and reflections. These distinguish texture vocabulary from optional modern rendering; the photo mapping above is this project's interpretation, not an official preset.
