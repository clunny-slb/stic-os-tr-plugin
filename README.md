# STIC-OS Team Relay — releases

Release channel for the **STIC-OS Team Relay** Obsidian plugin: real-time collaborative
editing in Obsidian against a self-hosted relay.

This repository holds **releases only** — no source. Each release carries the files Obsidian
needs and nothing else.

## Install with BRAT — recommended, desktop and mobile

1. Install **BRAT** (*Obsidian42 - BRAT*) from Obsidian's community plugins.
2. In BRAT's settings choose **Add beta plugin** and enter:

   ```
   clunny-slb/stic-os-tr-plugin
   ```

3. Enable **STIC-OS Team Relay** under *Community plugins*.

No token is required. BRAT checks for new releases when Obsidian starts, so updates arrive
on their own — this is the only channel that updates itself, on either platform.

## Install manually — desktop alternative

Download `stic-os-team-relay-<version>.zip` from the
[latest release](https://github.com/clunny-slb/stic-os-tr-plugin/releases/latest) and unzip
it into your vault's `.obsidian/plugins/` directory.

The archive expands to a single `stic-os-team-relay/` folder. **Do not rename it** —
Obsidian matches the folder name against the plugin id, and a renamed folder means the
plugin never appears in the list at all. Restart Obsidian, then enable the plugin.

Manual installs do not update themselves; repeat the download for each new version.

## What is in a release

| Asset | Purpose |
|---|---|
| `main.js`, `manifest.json`, `styles.css` | the plugin itself — what BRAT installs |
| `stic-os-team-relay-<version>.zip` | the same three files, packaged for manual install |
| `release.json` | version metadata and SHA-256 checksums for each file |

Verify a download against `release.json` with `shasum -a 256 <file>`.

## First run

The plugin talks to a relay control plane and ships with its deployment's server as the
default. On first use it will prompt you to sign in; you need an account on that server.

## Licence

MIT — see [`LICENSE`](LICENSE). Based on
[Relay](https://github.com/No-Instructions/Relay) by No Instructions, LLC.
