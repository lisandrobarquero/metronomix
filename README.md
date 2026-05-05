# Metronomix

Drummer practice metronome — web app built with vanilla JS + Web Audio API.

## Branches

| Branch | Description |
|---|---|
| `main` | v0.5 — Stable production app |
| `v1-engine` | v1.0 — Engine refactor in progress |

## Architecture (v1.0)

Clean separation of layers — engine has zero DOM references:

```
AudioEngine          → Web Audio, no DOM
MetronomeEngine      → Single scheduler, callbacks
M1Mode               → Phase shift, silent bars, subdivision
M2Mode               → Grid pattern, reference beat
M3Mode               → Play/silent phases, tap accuracy
SessionEngine        → Steps, rounds, rests
SceneService         → localStorage persistence
LatencyService       → Bluetooth delay
Metronomix           → Entry point — wires all layers
```

## Stack

- Vanilla JS (no framework)
- Web Audio API
- localStorage
- iOS Safari compatible

## Deploy

Hosted on GitHub Pages — `main` branch is production.