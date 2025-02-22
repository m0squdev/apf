# apf

An interface based on fzf for managing official repos, AUR and Flatpak packages on Arch Linux. apf provides a unified terminal UI for installing, removing and viewing packages from multiple sources.
It is basically a mix of yay (A)UR helper, (P)acman and (F)latpak!

## Features

- Interactive package selection using fzf
- Unified management of official repos, AUR and Flatpak packages
- Real-time package information preview
- Color-coded package sources
- Support for both system-wide and user-wide Flatpak installations
- Multi-package selection support

## Prerequisites

- flatpak
- fzf
- yay

## Installation

Make the script executable:
```bash
chmod +x apf
```

Move it to `~/.local/bin` (user-wide installation) or `/usr/bin` (system-wide installation).

## Usage

```bash
apf [FLAGS]
```

- `-f`: Enable fuzzy search You can set the `APF_FUZZY_SEARCH` environment variable to enable it by default
- `-h`: Display help message and exit
- `-u`: Install Flatpak packages user-wide instead of system-wide. You can set the `APF_FLATPAK_USER` environment variable to enable it by default

Press Tab to select multiple packages and press Enter to confirm your selection. Already installed packages will be removed and new packages will be installed.
