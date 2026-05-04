# Metronomix

Drummer practice metronome — web app built with vanilla JS + Web Audio API.

## Versions

| Version | Description |
|---|---|
| [v0.5](v0/) | Stable production app |
| [v1.0](v1/) | New architecture — engine refactor |

## Architecture (v1.0)

Clean separation of layers — engine has zero DOM references:

```
AudioEngine          → Web Audio, no DOM
MetronomeEngine      → Scheduler, callbacks
M1Mode / M2Mode / M3Mode → Mode strategies
SessionEngine        → Steps, rounds, rests
SceneService         → localStorage persistence
LatencyService       → Bluetooth delay
Metronomix           → Entry point
```

## Deploy

Hosted on GitHub Pages. Push to `main` to deploy.

## Stack

- Vanilla JS (no framework)
- Web Audio API
- localStorage
- iOS Safari compatible
