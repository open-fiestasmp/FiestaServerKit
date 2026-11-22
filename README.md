# minecraft server starter config

A small starting point for a Java Paper server, based on what we learned running FiestaSMP. Check each setting against your Paper and Minecraft version before using it.

1. Install a compatible Java runtime and Paper server from their official sources. Accept Mojang’s EULA only if you agree to it.
2. Stop the server. Back up your current `server.properties` and put the example in your server directory as `server.properties`.
3. Change the server name and player limit, then start Paper and check its console. Paper generates its own additional config files on first start.
4. If using a proxy, configure Paper and the proxy together using the official Paper proxy documentation. Restrict backend access to the proxy and set up forwarding before accepting traffic.

The example uses Minecraft account authentication. If you need offline accounts, set up a suitable authentication plugin and carefully secure the backend before changing that setting. Keep passwords, keys, IP addresses and generated credentials out of public repositories.

This is a community template, not an official Mojang or Paper project. No server software or Minecraft license is included.
