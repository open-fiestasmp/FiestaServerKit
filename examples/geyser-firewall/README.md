# Geyser ports and firewalls

Open the ports that match Geyser’s configured transport on both the host firewall and the cloud firewall. Fiesta’s Oracle proxy currently uses Geyser port `19132`, `transport: both`, and WebRTC port `19133`.

| Service | Protocol | Port |
|---|---|---:|
| Java proxy | TCP | 25565 |
| Geyser signaling | TCP | 19132 |
| Geyser gameplay | UDP | 19132 |
| WebRTC | UDP | 19133 |

For a public OCI server, add an ingress rule for each protocol and port. Use `0.0.0.0/0` only when players need to connect from anywhere; use a narrower source range when access is limited. Add matching IPv6 rules if the server accepts IPv6 traffic.

On Ubuntu with UFW, the matching rules are:

```sh
sudo ufw allow 25565/tcp
sudo ufw allow 19132/tcp
sudo ufw allow 19132/udp
sudo ufw allow 19133/udp
sudo ufw status
```

Do not expose Paper or queue backend ports to the public internet. Keep them on loopback, a private network, or an authenticated tunnel, and let the proxy reach them. For networks that accept offline accounts, use trusted proxy forwarding and keep its shared secret private; see the [Velocity and Paper example](../velocity-paper/README.md).

A port rule alone does not prove Bedrock can join. Test from an external Bedrock client after changing the Geyser configuration or firewall. Geyser’s [port-forwarding guide](https://geysermc.org/wiki/geyser/port-forwarding/) explains the TCP signaling, UDP gameplay, and WebRTC port requirements.
