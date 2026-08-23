# Blockbound

Blockbound is a standalone browser voxel sandbox game built with Three.js. Explore a procedurally generated world, gather resources, craft tools, build with blocks, and survive the night.

This is an independent project and is not affiliated with Mojang Studios or Microsoft.

## Run locally

The game is a single HTML file. Serve the project directory over HTTP because the game loads Three.js as an ES module:

```bash
python3 -m http.server 4173
```

Open <http://localhost:4173/index.html> in a modern browser.

## Controls

- Click **Enter the world** to start and capture the mouse
- `W` `A` `S` `D`: move
- Mouse: look around
- `Space`: jump
- `Shift`: sprint
- Left click: mine blocks or attack hostile mobs
- Right click: place the selected block
- `1` through `9`: select a hotbar slot
- `E`: open inventory and crafting
- `Esc`: close the inventory or release pointer lock

## Features

- Procedural terrain with meadow, forest, and desert biomes
- Chunk-based voxel rendering with an 8-chunk render radius
- Procedural pixel-art textures generated with the Canvas API
- Nine-slot hotbar and expandable inventory
- Wood, planks, crafting tables, and wooden pickaxe crafting
- Day/night lighting cycle with a visible sun
- Hostile night mobs, combat, health, respawn, and block-break particles
- Compact localStorage saves for player state, inventory, time, and block edits
- No external image assets

## Development

The game lives in [`index.html`](./index.html), with CSS and JavaScript embedded in the file. Three.js is loaded from its jsDelivr CDN import.

For browser smoke testing, the project can be served locally and driven with Playwright using the system Chromium installation.

## License

The project code is released under the MIT License. See [`LICENSE`](./LICENSE).

Three.js is used under its own MIT License: <https://github.com/mrdoob/three.js/blob/dev/LICENSE>.
