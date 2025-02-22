# fzfpkg

A fuzzy-finder interface for managing official repos, AUR and Flatpak packages on Arch Linux. fzfpkg provides a unified terminal UI for installing, removing and viewing packages from multiple sources.

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
chmod +x fzfpkg
```

Move it to `~/.local/bin` (user-wide installation) or `/usr/bin` (system-wide installation).

## Usage

```bash
fzfpkg [FLAGS]
```

- `-h`: Display help message and exit
- `-u`: Install Flatpak packages user-wide instead of system-wide. You can also set the `FZFPKG_FLATPAK_USER` environment variable to achieve the same result

Press Tab to select multiple packages and press Enter to confirm your selection. Already installed packages will be removed and new packages will be installed.
