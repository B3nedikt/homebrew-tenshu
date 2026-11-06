# Tenshu for Mac — Homebrew tap

The Tenshu desktop apps, as notarized Developer ID builds. Apple silicon, macOS 14 (Sonoma) or later.

```bash
brew tap b3nedikt/tenshu
brew install --cask tenshu-control
```

Install **Tenshu Control first**: every other app needs it. Control also comes from the Mac App
Store; if you have that copy, keep it and install only the other apps from here. Don't install a
second Control.

| Cask | App |
|---|---|
| `tenshu-control` | Tenshu Control: sync and encryption keys for the Tenshu apps |
| `tenshu-drive` | Tenshu Drive: encrypted file storage |
| `tenshu-photos` | Tenshu Photos: encrypted photo library |
| `tenshu-calendar` | Tenshu Calendar |
| `tenshu-contacts` | Tenshu Contacts |
| `tenshu-fit` | Tenshu Fit: workouts and health |
| `tenshu-maps` | Tenshu Maps: offline maps of your places |
| `tenshu-timeline` | Tenshu Timeline: location history |
| `tenshu-home` | Tenshu Home: smart-home devices and automations |
| `tenshu-mia` | Tenshu Mia: ask questions about your Tenshu data |

All apps are released together at one version. Update with `brew upgrade --cask`.
`brew uninstall --cask tenshu-control --zap` also removes this Mac's Tenshu data and keys.

The casks are generated from the release manifest by `scripts/macos-direct-publish.sh --casks` in
the Tenshu repository. Edit the generator there, not these files. Each cask pins the sha256 of its
download from `releases.tenshu.app`.
