# Runtime notes

Podex is an overlay around a local Codex CLIProxy install. The repository is intentionally separate from both the official app bundle and the operator's private seat data.

## Remote Control

Remote Control has two independent prerequisites:

1. The custom desktop session must be signed in to ChatGPT so its Connections settings can load.
2. The Codex app-server must be able to create its local control socket.

Seat `CODEX_HOME` directories live under `~/.codex-cliproxy/<seat>` so the macOS Unix-socket path stays below `SUN_LEN`. The old long support directories remain the durable backing store through narrow symlinks; the `app-server-control` directory is recreated locally for each short home.

The local switchboard listens only on loopback at `127.0.0.1:8369`, rejects untrusted browser origins, and does not return raw seat paths.

## Seats

The active machine-local seat registry is outside this repository:

```text
~/Library/Application Support/Codex CLIProxy Seats/seats.json
```

To authenticate an isolated CLI seat, run:

```bash
~/.local/bin/codex-cliproxy-seat login work
```

The desktop ChatGPT session for that seat still needs to be signed in through the custom app's own login flow. The regular `/Applications/ChatGPT.app` session is never copied or modified.

## Safe activation

The installed proxy currently hosts live Codex work. The ASAR candidate is therefore verified but not hot-swapped during an active task; the custom launcher default is already installed so the next launch selects the short Personal home. When handing off safely, restart only `/Applications/Codex CLIProxy.app`; the regular ChatGPT app is out of scope.
