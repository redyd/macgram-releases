<div align="center">

<img src="logo.png" alt="" width="112">

# macgram

**An entity-relationship diagram editor (Merise / UML) whose files version cleanly with git.**
An alternative to Looping, for Linux and Windows.

[![Latest version](https://img.shields.io/github/v/release/redyd/macgram-releases?label=version&color=1565C0)](https://github.com/redyd/macgram-releases/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/redyd/macgram-releases/total?label=downloads&color=1565C0)](https://github.com/redyd/macgram-releases/releases)

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="screenshot-dark.png">
  <img src="screenshot-light.png" alt="A Customer – Order – Line – Product diagram in macgram, its relational model generated underneath, and the assistant adding an entity in the side panel" width="860">
</picture>

</div>

## Download

These links always point to the latest version.

| System | File | |
|---|---|---|
| **Windows** | Installer | [macgram-windows-x64-setup.exe](https://github.com/redyd/macgram-releases/releases/latest/download/macgram-windows-x64-setup.exe) |
| | Portable zip, no installation | [macgram-windows-x64.zip](https://github.com/redyd/macgram-releases/releases/latest/download/macgram-windows-x64.zip) |
| **Linux** | AppImage, any distribution | [macgram-x86_64.AppImage](https://github.com/redyd/macgram-releases/releases/latest/download/macgram-x86_64.AppImage) |
| | Debian, Ubuntu, Mint | [macgram-amd64.deb](https://github.com/redyd/macgram-releases/releases/latest/download/macgram-amd64.deb) |
| | Fedora | [macgram-x86_64.rpm](https://github.com/redyd/macgram-releases/releases/latest/download/macgram-x86_64.rpm) |
| | Archive | [macgram-linux-x64.tar.gz](https://github.com/redyd/macgram-releases/releases/latest/download/macgram-linux-x64.tar.gz) |

Earlier versions are on the [Releases](https://github.com/redyd/macgram-releases/releases) page. There is no macOS build yet.

## Install

**Windows.** Run the installer. It is not signed, so Windows may show "Windows protected your PC": click *More info*, then *Run anyway*.

**AppImage.**

```bash
chmod +x macgram-x86_64.AppImage
./macgram-x86_64.AppImage
```

**Debian, Ubuntu, Mint.**

```bash
sudo apt install ./macgram-amd64.deb
```

**Fedora.**

```bash
sudo dnf install ./macgram-x86_64.rpm
```

**Archive.** Extract it anywhere and run `./macgram`; the binary needs the `lib/` and `data/` folders next to it.

The `.deb` and `.rpm` packages add `macgram` to the application menu and to the `PATH`. A file can be given as an argument: `macgram model.mcd.json`.

## Updates

The app looks for a new version when it starts and offers to install it. Nothing is downloaded without your say.

| Installation | What "Update" does |
|---|---|
| Windows installer | downloads the next installer and runs it |
| AppImage | replaces the AppImage file |
| `.deb`, `.rpm` | downloads the package and installs it (the system asks for your password) |
| Portable zip, `.tar.gz` | opens this page |

## What macgram does

- **The conceptual model**: entities, binary or n-ary associations, cardinalities, weak entities, enums, notes and annotation arrows, in Merise or UML notation.
- **The relational model, live**: tables, primary and foreign keys are generated under the diagram as you draw.
- **Files made for git**: JSON with one element per line and random ids, so diffs stay readable and branches merge without collisions.
- **Automatic layout**: one button moves the boxes around to keep links from crossing.
- **An AI assistant**: talk to Claude Code or Codex in the side panel and watch it draw, one undoable step at a time. It runs the CLI already installed and signed in on your machine; macgram holds no key. A local MCP server lets an AI started from your terminal join in too.
- **Looping import**: `.loo` files open directly.
- **Export** to PNG and SVG, in the light or dark theme.
- **And the rest**: undo / redo, copy and paste, search by name, strict mode, interface in English or French.

## Something wrong?

Open an [issue](https://github.com/redyd/macgram-releases/issues) with your system and the version (it is shown in the toolbar).

## License

macgram is distributed under the MIT license with the *Commons Clause*: free to use, at work too, but not to resell. This repository only holds the files to download.
