# fiesta stack snapshot

Checked 2026-11-26. This describes Fiesta's current layout, not a ready-made install. Verify versions and settings against the server before copying anything.

- Oracle hosts the authoritative Paper game world. Its current settings allow 20 players, use offline account mode, and set view and simulation distance to 32. AuthMe handles the in-game login step; offline mode still requires a correctly secured proxy and backend.
- Oracle also runs the Velocity entry proxy, a separate Paper queue world, and the shared queue coordinator. Queue inventory and player state are separate from the main game.
- A Luna proxy and waiting service are being used as a remote edge path back to Oracle. They do not host a second copy of the world. High client ping and reconnect failures have been reported, and a healthy server-side probe does not verify the route from a player's network.
- The main game, proxy, queue, and queue coordinator services were active at the time of this check. Chunky generation is paused and automatic world-tier eviction is disabled while Oracle storage is tight.
- Fiesta's public entry currently reaches Oracle. Treat the Luna route as under evaluation until players confirm stable connections and lower ping.
- The plugin inventory is in [PLUGINS.md](PLUGINS.md). It records files and hashes; a JAR in a folder does not prove it loaded. Fetch third-party plugins from their publishers and check compatibility and license terms.

The public world snapshots live in separate repositories: [world](https://github.com/open-fiestasmp/world), [world-nether](https://github.com/open-fiestasmp/world-nether), [world-the-end](https://github.com/open-fiestasmp/world-the-end), and [world-maintaince](https://github.com/open-fiestasmp/world-maintaince). They are world backups, not complete server restores.

This kit leaves out credentials, passwords, private addresses, and live plugin databases. Keep those in a private backup. Do not put them in an example config or commit.
