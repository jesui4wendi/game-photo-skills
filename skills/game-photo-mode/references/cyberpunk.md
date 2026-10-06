# Cyberpunk 2077: scene-specific material and light

## Baseline

Aim for high-detail, real-time 3D Cyberpunk 2077-like environments and characters, not the Edgerunners anime or a generic purple neon illustration. Keep source camera and time of day. Daylight, domestic spaces and quiet service yards also belong in this world.

The [official art-direction notes](https://www.cyberpunk.net/en/news/28441/c-usb-01-backup-concept-art-cp-visual-styles) distinguish four visual languages. Select one primary language from the photograph, with another only as a restrained accent:

| Language | Appropriate context | Useful translation |
| --- | --- | --- |
| Entropism | Modest residences, service alleys, utilitarian rooms | Repaired concrete, mismatched bolted panels, exposed practical cables, weathered paint; place retrofit details on existing architecture |
| Kitsch | Shops, nightlife, bright street clothing | Scuffed coloured molded plastic, local saturated colour, modest luminous accents; preserve the source outfit and silhouette |
| Neomilitarism | Corporate lobbies, sharp architecture, uniform-like clothing | Cold precise hard surfaces, controlled dark metal, angular utilitarian details; avoid adding guns or turning civilians into soldiers |
| Neokitsch | Luxury rooms, rich landscaping or upscale clothing | Contrasting polished luxury and natural materials, deliberate lighting; avoid replacing the entire original location |

The current demonstration tests Entropism and Entropism with Kitsch accents. The other two are documented routing guidance, not independently demonstrated presets.

## Translate the scene

Rebuild materials rather than tinting the original: authored weathered concrete panel faces; deliberately grouped service metal, grilles and access readers; hard-surface silhouettes; roughness differences between paint, glass, metal, skin and fabric. Any added fixture should be physically attached to an existing object, correctly scaled and purposeful.

For a person, retain facial features, hair, gaze, pose, body proportions, coat colour and object held. Subtle technical seams or reinforced fabric are optional contextual changes; extensive cyberware, replacement limbs or a new costume require the user's request. Check hands and face after rendering.

Tie reflections to visible sources. Dusk may use amber windows with local cool shelter lights and rough wet asphalt. An overcast courtyard uses cool ambient light and a small warm doorway lamp. Avoid making every surface cyan-magenta or converting every daytime photo to midnight. Exposure must keep the subject readable.

Do not insert a famous skyline, franchise protagonist, branded billboard, HUD or weapon to compensate for weak rendering. The official design language should guide materials, layout detail and lighting; recognizability cannot be proved by a logo.

## Typical failures and narrow repairs

- Ordinary photo with coloured lights: describe concrete / metal retrofit construction and actual PBR-like texture density, then reconstruct those surfaces.
- Generic dystopian alley: group functional details and contrast rough utilitarian surfaces with a few appropriate accents; preserve source scene identity.
- Face replaced by another person: re-anchor to the original face and pose; remove optional outfit changes before increasing style strength.
- Universal night-neon conversion: restore the original time of day and localise emissive light to physical fixtures.

Source: [official visual styles](https://www.cyberpunk.net/en/news/28441/c-usb-01-backup-concept-art-cp-visual-styles), [official game / media portal](https://www.cyberpunk.net/us/en/). The mappings above are this project's artistic interpretation. No official assets are bundled.
