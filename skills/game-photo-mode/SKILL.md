---
name: game-photo-mode
description: Edit a supplied photograph into a Minecraft default-texture block world or a Cyberpunk 2077 game-like scene while retaining its layout and subjects. Use for 照片转我的世界、Minecraft 方块材质、赛博朋克2077照片风格. Requires an image-editing-capable host; outputs images, not playable worlds or asset packs.
license: MIT
---

# Game Photo Mode

Rebuild the supplied photograph in a game's visual language. Change geometry, materials and rendering together, with the source photograph passed as the actual edit input.

## Choose the recipe

- Minecraft / 我的世界: read [minecraft.md](references/minecraft.md). Default to Java-style default textures and simple vanilla lighting. A user's screenshot or explicitly requested graphics mode overrides this baseline.
- Cyberpunk 2077 / 赛博朋克2077: read [cyberpunk.md](references/cyberpunk.md). Choose the design language from the source setting; retain its time of day unless the user requests a change.
- Another title: these two recipes do not establish support for it. Research its specific edition, gameplay captures and art direction, then prepare a clearly labelled experimental edit. Do not quietly borrow one of these looks or claim the new mode is validated.

## Anchor the edit

Inspect the original first. Record its aspect ratio, viewpoint, subject count, positions, pose, silhouette, dominant clothing colours, important landmarks and object classes. Put those specific invariants in the prompt. A person's face can retain likeness in realistic Cyberpunk rendering; Minecraft's block face can only carry coarse cues such as skin tone, hairstyle, outfit colours and pose. Do not promise exact facial likeness after converting a face to a few flat pixels.

Use the host's image editor. In Codex use the built-in image tool: inspect a local input before editing, include its path if supported, or use the smallest recent-image set that contains the target. Label a user-provided game screenshot as a style reference, never as another object to merge into the photo. Only use screenshots the user provides or a legitimately accessible reference; no extracted textures, meshes or characters are required.

When no photo is attached or accessible, ask for the input photo. Do not invent a replacement. If the host cannot edit images, explain that and return a ready-to-use prompt; a prompt is not an edited image. Do not silently switch to a paid API or install an unrelated image pipeline.

## Build the prompt

Use the chosen recipe to fill these fields with concrete observations:

```text
Use case: style-transfer.
Input image: supplied photograph, the edit target. Optional second image: style reference only.
Target: [game, edition / rendering baseline, scene-appropriate design language].
Keep: [aspect ratio, camera, source landmarks, subject count and pose, object positions and classes].
Rebuild: [map each important surface / object to the recipe's geometry and material vocabulary].
Rendering: [texture scale, shading, light sources, material response].
Avoid: [recipe-specific mismatches], new foreground subjects, unrelated landmarks, HUD, logos, watermark or invented readable signage.
Output: one edited image of the same scene.
```

Preserve the user's requested variations. Strong geometric stylization necessarily simplifies silhouettes and proportions; retain recognizability rather than pretending every pixel remains fixed. Do not add weapons, iconic characters, skyline landmarks or overlays merely to identify the game.

## Inspect, repair, deliver

Read [review.md](references/review.md) for the relevant visual checks. Compare the output and original together, at full composition and at material / face details. If a major requirement misses, make a targeted revision anchored to the original, repeating the invariants. The repair should identify the observed defect: for example, remove reflected windows from matte Minecraft paving, rather than asking for “more Minecraft”. After two unsuccessful targeted revisions, report the remaining mismatch instead of calling the result a match.

Return the actual image. Save beside the input or to the user's chosen directory with a new filename such as `photo-minecraft.png` or `photo-cyberpunk.png`; preserve originals and existing versions. Keep the explanation short and in the user's language. Describe any visible compromise. A generated image is neither an official game screenshot nor an engine render, and its resemblance is a visual judgement, not a numerical fidelity guarantee. Do not publish a user's photos or edits unless they ask.
