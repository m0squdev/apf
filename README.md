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

Usage: `apf [FLAGS]`

FLAGS:
- `-f`: Enable fuzzy search. Corresponding environment variable: `APF_FUZZY_SEARCH`
- `-h`: Print this message and exit
- `-r`: Recursively remove dependencies of AUR packages to remove. Corresponding environment variable: `APF_REMOVE_DEPENDENCIES`
- `-u`: Install Flatpak packages user-wide instead of system-wide. Corresponding environment variable: `APF_FLATPAK_USER`

Press Tab to select multiple packages and press Enter to confirm your selection. Already installed packages will be removed and new packages will be installed.
