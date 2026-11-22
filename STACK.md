# fiesta stack snapshot

This is what was observed on 2026-11-22. It is an inventory, not a complete install guide or a guarantee these versions work together on another server.

- Main game server reported Minecraft 1.21.11 with a development server build. Check the jar and plugin compatibility before copying its setup.
- The host Java command reported OpenJDK 25.0.5.1. Different services may need different Java versions.
- Fiesta runs a game server, Velocity proxy, queue server, shared queue coordinator, admin panel, chat archive and several moderation and join-review services.
- Luna has a proxy, a queue server and an SSH tunnel to the Oracle host.
- [The plugin list](PLUGINS.md) records jars found on both hosts, including versions when their metadata supplied them. A jar in the folder is not proof that it loaded.

World data, accounts, plugin databases, credentials and private network settings are separate from these templates. Fetch each third-party plugin from its own publisher and review its license and setup guide.
