# Pixelmon pack

packwiz pack for Los's "Pixelmon" server: Minecraft 1.16.5, Forge 36.2.34, with Pixelmon 9.1.10 (client build from CurseForge, same version as the server), FallingTree 2.11.7 and The Warp Mod 0.0.2. Links only, no mod files.

Server: `dorkunify.duckdns.org:25566` (at home or on the VPN: `10.24.4.143:25566`). Whitelisted players only; send Los your Minecraft username first.

## Quick setup (one command)
Close Prism Launcher first.

Windows (PowerShell):

    irm https://raw.githubusercontent.com/loswastaken/pixelmon-pack/main/join.ps1 | iex

macOS / Linux:

    curl -fsSL https://raw.githubusercontent.com/loswastaken/pixelmon-pack/main/join.sh | bash

It installs Prism Launcher if needed, creates (or refreshes) the "Pixelmon" instance, sets up the mod sync and adds the server. Then open Prism, sign in with your Microsoft account, and press Play. Read `join.ps1` / `join.sh` first if you like; they only touch Prism's own folder.

## Hand downloads
- **OptiFine 1.16.5 HD U G8** (optional, recommended): the script asks, opens https://optifine.net/adloadx?f=OptiFine_1.16.5_HD_U_G8.jar and picks it up from your Downloads folder (checksum-checked). OptiFine can't be linked in a pack, so it's never synced automatically.

## Manual setup
1. Create a Prism instance named "Pixelmon": Minecraft 1.16.5, Forge 36.2.34 (Java 8).
2. Download https://github.com/packwiz/packwiz-installer-bootstrap/releases/latest/download/packwiz-installer-bootstrap.jar into the instance's `.minecraft` folder.
3. Instance Settings > Custom commands > Pre-launch command:
   `"$INST_JAVA" -jar packwiz-installer-bootstrap.jar https://raw.githubusercontent.com/loswastaken/pixelmon-pack/main/pack.toml`
4. Launch. Mods sync on every launch.
