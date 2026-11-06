# cfrelay-masque (linux/amd64)

Single-file Go client that exposes a Cloudflare WARP MASQUE (HTTP/2) exit as a
VLESS-over-WebSocket proxy through a self-hosted Cloudflare Worker.

| | |
|---|---|
| Binary | `cfrelay-masque-linux-amd64` |
| Platform | Linux amd64, static (CGO_ENABLED=0) |
| SHA256 | `c7a5f28305f4643e817b091b9ed16ddebcb4a87b60b69259f08deb5a5faabb3e` |
| Built from | `cfrelay-masque` project, Go 1.26 |

Download and verify:

```sh
curl -fL -o cfrelay-masque \
  https://raw.githubusercontent.com/wzbtcbkrsz/ADBlock-Rules/master/cfrelay-masque/cfrelay-masque-linux-amd64
chmod +x cfrelay-masque
echo 'c7a5f28305f4643e817b091b9ed16ddebcb4a87b60b69259f08deb5a5faabb3e  cfrelay-masque' | sha256sum -c -
```

Running it requires credentials supplied by the relay operator
(relay agent token, the WARP `masque://` URI, and a VLESS UUID).
Pass them via environment variables — never commit them.

Configuration and startup instructions are in the `cfrelay-masque-client`
skill shipped with the project.
