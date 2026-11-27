# fiesta server kit

A starting point for a Java Paper server, plus an inventory of what Fiesta was running. These examples need changes for your own server and software version.

- [Server settings](server.properties.example): copy to `server.properties` with the server stopped, then edit.
- [Plugin inventory](PLUGINS.md): names, versions where available and hashes for the game server, proxies and queues.
- [Plugin source links](UPSTREAMS.md): upstream links and notes for the plugins we could identify; no third-party jars are included.
- [MiniMOTD example](examples/minimotd/main.conf.example): a sanitized MOTD and displayed-count setup for MiniMOTD 2.2.5.
- [Velocity and Paper forwarding](examples/velocity-paper/README.md): a modern-forwarding example, backend firewall rules, and notes for networks that use offline accounts.
- [Geyser and firewall ports](examples/geyser-firewall/README.md): OCI ingress and UFW rules for the current Geyser transport.
- [Fiesta stack](STACK.md): what the hosts were running when checked.
- [Performance notes](PERFORMANCE.md): a few things to watch when tuning.

Install compatible Java and Paper from their official sources and accept the Minecraft EULA only if you agree to it. Back up existing config before replacing it. Paper creates its other settings on first start.

The `server.properties` file here is for a standalone server listening on the Java port. For Paper behind Velocity, use the backend listener settings in the [forwarding example](examples/velocity-paper/README.md) instead: bind Paper to loopback on its private backend port, and do not expose that port to players.

The example uses Minecraft account authentication. If you allow offline accounts, arrange account authentication and secure your backend before changing that setting. Keep passwords, keys and addresses out of public repos.

Community project; not an official Mojang or Paper product. No Minecraft license or server binaries are included.
