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

The example above has Velocity authenticate accounts. For offline accounts, set `online-mode = false` in Velocity, install AuthMe on the backends that handle login, and install the matching AuthMeVelocity plugin on the proxy. Keep Paper's Velocity forwarding enabled. Fiesta currently pairs Velocity `online-mode = false` with modern forwarding to Paper 1.21.11; check the AuthMe guide for the exact forwarding setup supported by your versions before copying that combination.

For this profile, keep `server.properties` at `online-mode=false` and set Paper's Velocity `online-mode` flag to `false` too:

```yaml
proxies:
  velocity:
    enabled: true
    online-mode: false
    secret: "replace-with-your-private-velocity-forwarding-secret"
```

On each AuthMe backend, enable the proxy hook and turn off the database cache:

```yaml
Hooks:
  bungeecord: true
  proxySharedSecret: "replace-with-a-private-authme-secret"

DataSource:
  caching: false
```

In the AuthMeVelocity config, use the same AuthMe secret and keep unauthenticated players from switching to protected servers or running commands:

```yaml
authServers:
  - main
proxySharedSecret: "replace-with-the-same-private-authme-secret"
serverSwitch:
  requiresAuth: true
commands:
  requireAuth: true
chatRequiresAuth: true
```

The AuthMe secret is separate from Velocity's forwarding secret. Don't reuse one value for both. `authServers` must use names from `velocity.toml` and should list servers where AuthMe handles login. `chatRequiresAuth: false` permits pre-login chat on the proxy's auth servers; it is not a queue-only switch. Use that only when you intend to allow pre-login chat, and handle queue moderation separately.

Keep both secrets out of public repositories. Follow AuthMe's current guide for the forwarding mode and login redirects supported by your release. Test registration, login, queue entry, server switches, and reconnects with your exact versions before opening the network to players.

References: [Velocity forwarding](https://docs.papermc.io/velocity/player-information-forwarding/), [Velocity server security](https://docs.papermc.io/velocity/security/), [Paper global configuration](https://docs.papermc.io/paper/reference/global-configuration/), and [AuthMe proxy setup](https://github.com/AuthMe/AuthMeReloaded/wiki/Proxy-Configuration).
