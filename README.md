# ScryRPG Connected Campaign for Foundry VTT (alpha)

> **Alpha build. Not a finished release.** This is an early test version of the ScryRPG module
> for Foundry VTT, published for the ScryRPG closed beta. It can damage a Foundry world. Back up
> your world before you install it, and before each session while you use it. Use it on a copy
> of your world if you can.

The module adds a ScryRPG campaign panel and character sheet inside Foundry, and keeps linked
characters in step with the [ScryRPG](https://scryrpg.com) website: inventory and containers,
the party stash, coins, shops, loot, the library, and history with undo.

## Who can use it

It only connects for ScryRPG parties that have been invited to the closed beta. Without an
invitation you can install it, but it won't connect to ScryRPG.

## Requirements

- Foundry VTT 13 with D&D 5e 5.3.x, or Foundry VTT 14 with D&D 5e 5.3.x or 6.0.x.
- Foundry reached over an `https://` address (or `localhost`).
- A ScryRPG account for every person at the table.

## Install

1. On Foundry's Setup screen, open **Add-on Modules** and click **Install Module**.
2. Paste this link into **Manifest URL** and click **Install**:

   ```
   https://github.com/bmikk/scryrpg-foundry-releases/releases/latest/download/module.json
   ```

The full setup, backup and troubleshooting steps are in the [guide](GUIDE.md), which also ships
inside the module as its README.

## What's here

This repository holds only the released builds, the guide and the license. Each release has two
files: `module.json` and `module.zip`. The source code is not published here.

## License

MIT; see [LICENSE](LICENSE).
