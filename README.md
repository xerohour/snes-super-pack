# snes-super-pack

"Super pack, with save function" — a Super SNES emulator pack built with
Pocket, by Felipe Reis (Instagram @_felipereiscruz).

- Source Pocket project: https://madewithpocket.com/p/FmbdciytZ
- Live mirror: https://xerohour.github.io/snes-super-pack/

9 games, all loaded from images bundled under `assets/` (the emulator core
and each ROM are encoded as pixel data inside the PNGs, decoded at runtime
with canvas `getImageData`):

- Donkey Kong Country (ROM A, 2 images)
- The Legend of Zelda: A Link to the Past (ROM B)
- Super Bomberman 5 (ROM C)
- Super Mario World (ROM D)
- Super Mario Kart (ROM E)
- Mega Man X (ROM F)
- Aladdin (ROM G)
- Street Fighter II Turbo (ROM H, 2 images)
- Ultimate Mortal Kombat 3 (ROM I, 2 images)

Single self-contained `index.html` (React 19 + Nostalgist / snes9x core)
plus 15 local images. The original Facebook CDN links expire, so every
image was downloaded and localised — the page has no expiring external
references and makes no network calls of its own.

Saves (save states + SRAM) are stored in the browser's own IndexedDB
(`snes-rom-db`), so they work on this static host exactly as in Pocket.
No server, no multiplayer, no backend.
