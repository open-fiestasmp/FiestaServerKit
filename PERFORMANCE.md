# keeping the server smooth

Start with a view distance around 10 and simulation distance around 6, then adjust after looking at tick times, memory and player feedback. These are starting points, not a promise that they will fit every server. Large view distances load many more chunks per player.

Generate new chunks during a quiet window and keep free disk space. Watch tick time and storage while any map renderer or backup is running. If the server is struggling, pause background work and check a profiler before changing a bunch of settings.

The [plugin inventory](PLUGINS.md) lists what Fiesta used at the time of the snapshot. Install only what you actually need, and follow each plugin's own version and setup instructions.
