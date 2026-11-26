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

The example above has Velocity authenticate accounts. For `online-mode = false`, install AuthMe on the backend that handles login and the matching AuthMe Velocity plugin on the proxy. On each AuthMe backend, enable the proxy hook and disable the database cache:

```yaml
Hooks:
  bungeecord: true
  proxySharedSecret: "set-the-same-private-random-value-on-the-proxy"

DataSource:
  caching: false
```

Set the same private `proxySharedSecret` in the Velocity plugin config. Its `authServers` list should contain only backend names where AuthMe actually runs. Keep the secret out of public repositories. Follow AuthMe's current guide for the forwarding mode and login redirects supported by your release. Test account registration, login, queue access, server switches, and reconnects on a staging setup before opening it to players.

References: [Velocity forwarding](https://docs.papermc.io/velocity/player-information-forwarding/), [Velocity server security](https://docs.papermc.io/velocity/security/), [Paper global configuration](https://docs.papermc.io/paper/reference/global-configuration/), and [AuthMe proxy setup](https://github.com/AuthMe/AuthMeReloaded/wiki/Proxy-Configuration).
