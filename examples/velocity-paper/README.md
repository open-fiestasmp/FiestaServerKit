# Paper behind Velocity

This is a small modern-forwarding example for a Paper backend and a Velocity proxy. The code blocks are setting snippets, not complete configuration files. Check the docs for the versions you install.

## Velocity

Add the matching settings to `velocity.toml`:

```toml
bind = "0.0.0.0:25565"
online-mode = true
player-info-forwarding-mode = "modern"
forwarding-secret-file = "forwarding.secret"

[servers]
main = "127.0.0.1:25566"
try = ["main"]
```

Keep `forwarding.secret` private. Generate a new random value for each network and copy it into Paper's Velocity secret setting. Never reuse this example or publish the actual value.

## Paper backend

For a proxy on the same host, bind the backend to loopback and turn off backend authentication:

```properties
server-ip=127.0.0.1
server-port=25566
online-mode=false
```

In `spigot.yml`, leave legacy forwarding disabled:

```yaml
settings:
  bungeecord: false
```

In `config/paper-global.yml`, enable Velocity forwarding and use the same secret as the proxy:

```yaml
proxies:
  velocity:
    enabled: true
    online-mode: true
    secret: "replace-this-with-your-private-forwarding-secret"
```

If the proxy and backend are on different hosts, use a private network or authenticated tunnel and allow the backend port only from the proxy. Modern forwarding adds a signed forwarding check; it does not replace a firewall. Check both the cloud firewall and the host firewall.

## Networks using offline accounts

This example has Velocity authenticate accounts and is for a network using Minecraft account authentication. If the proxy instead uses `online-mode = false`, configure authentication on the backend and make Paper's Velocity `online-mode` value match the proxy. AuthMe's proxy integration has its own setup for that mode; follow its current guide and use one forwarding method consistently. Test login, server switches, and backend isolation on a staging server before opening it to players.

References: [Velocity forwarding](https://docs.papermc.io/velocity/player-information-forwarding/), [Velocity server security](https://docs.papermc.io/velocity/security/), [Paper global configuration](https://docs.papermc.io/paper/reference/global-configuration/), and [AuthMe proxy setup](https://github.com/AuthMe/AuthMeReloaded/wiki/Proxy-Configuration).
