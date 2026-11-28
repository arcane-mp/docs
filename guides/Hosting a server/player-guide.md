---
title: Player guide
description: Install the ArcaneMP client, join a server, keep the client updated, and report a bug. The page to send your players.
sidebar:
  order: 930
---

This page is for players. You do not compile anything, install server resources or set up a database: you install the client once, and the launcher keeps it up to date. Server owners can send their players here; setting up a server is covered in [Hosting a server](/guides/hosting-a-server/run-a-server/).

ArcaneMP is pre-release software, so expect rough edges.

## What you need

- A Windows PC that runs Hogwarts Legacy.
- Your own PC copy of Hogwarts Legacy from Steam or the Epic Games Store. A PC Game Pass copy also works, but its support is experimental. Keep the game updated to the version the release asks for.
- Free disk space for the extracted client and its later updates.
- An internet connection for updates, the server list and playing.

## Install the client

1. Join the [ArcaneMP Discord](https://discord.gg/RzqENjGe99) and download the complete release ZIP from its `#releases` channel. Download your own copy there even when a server owner invited you, and never use a client someone else copied, changed or re-uploaded.
2. Extract the whole archive. Do not run anything from inside the ZIP.
3. Keep the extracted `client/` directory in a permanent folder your Windows account can write to. It does not go inside the Hogwarts Legacy directory.
4. Keep every file in it together: `ArcaneMPLauncher.exe`, `ArcaneMPClient.dll`, `MafiaHubUpdater.exe`, `cef_subprocess.exe` and the browser runtime files around them.
5. Run `ArcaneMPLauncher.exe`.

Each time it starts, the launcher checks its release channel for an update before it starts the game. The updater may close and reopen the launcher while it replaces files. Let it finish, and do not start a second copy in the meantime.

## Join a server

In the launcher, open **Play** and pick a server from the list, or enter the address the server owner gave you. The client uses port 27015 unless the address ends in `:port`, so add one only when the server owner says the server uses another port. Fill **Password** only if the server has one.

A server owner can also send you a link such as `arcanemp://play.example.com`. Once you have started the launcher at least once, opening the link connects you straight to that server.

When you join, the server sends you its resources, and the join screen shows how much has downloaded and how fast. You never copy server resources into the client folder yourself. The first join to a server takes longer than later ones.

### Servers that require mods

Some servers require CurseForge mods. Your game installs the ones you are missing and updates the rest when you join. The game only changes its mods when it starts, so it may restart and join the server again by itself. Let it.

While you play on a server that requires mods, any mod you copied into the game's `Phoenix/Mods` folder by hand is moved to `Phoenix/ArcaneMP-ParkedMods` beside it. Nothing is deleted. A server that requires no mods leaves your mods where they are.

If a required mod cannot be installed, you are turned away before the world loads, with the cause on screen. [Rejected joins](/guides/hosting-a-server/configuration/#rejected-joins) lists each cause and what helps.

## Updates

After the first install, always start ArcaneMP with `ArcaneMPLauncher.exe`. It downloads later releases on its own. Never accept replacement client files from a server owner.

The launcher only updates your client. A server owner updates their server separately, so right after a release a server can still be on the old one for a while, and it turns away clients that do not match it.

Do not mix files from different releases. If an update stays broken, download the ZIP again and extract it into a new, empty folder instead of copying it over the old one.

## Common problems

| Problem | What to try |
| --- | --- |
| The launcher does not start | Extract the whole archive into a folder your account can write to, keep every file together, and do not run it from inside the ZIP. |
| The update check fails | Check your connection and try again. The launcher can start with the files it has, but a server may turn an outdated client away. |
| Hogwarts Legacy is not found | Make sure the game is installed and starts normally from its own store. |
| A server is missing from the list, or cannot be reached | Check the address and port with the server owner. Some servers are not listed and are only reachable by address. |
| You are turned away as soon as you connect | Restart the launcher so it can update. If you are already up to date, the server may still be on another release. |
| Loading stops after the download | Restart once. If it happens again, report it with your client log and the server's name. Do not copy resource folders into the client. |
| A required mod fails | See [Rejected joins](/guides/hosting-a-server/configuration/#rejected-joins). Antivirus folder protection and OneDrive are the usual causes. |

## Report a bug

A useful report has:

- what you were doing and what you expected to happen;
- roughly when it happened, with your time zone;
- the server's name or address;
- whether it happens every time;
- a screenshot or short video if the problem is visual;
- your client log, `logs/ArcaneMP.log` beside `ArcaneMPLauncher.exe`, taken right after the problem happened.

Never post server keys, passwords, sign-in details or other players' personal information. Bug reports and test coordination belong in the [ArcaneMP Discord](https://discord.gg/RzqENjGe99).
