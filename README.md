# apf

An interface based on fzf for managing official repos, AUR and Flatpak packages on Arch Linux. apf provides a unified terminal UI for installing, removing and viewing packages from multiple sources.
It is basically a mix of yay (A)UR helper, (P)acman and (F)latpak!

## Features

- Unified management of official repos and AUR packages (via yay) and Flatpak packages (via the flatpak CLI)
- Selection of multiple packages at once
- Filtering by installed packages
- Support for both system-wide and user-wide Flatpak installations
- Package information in sidebar

## Prerequisites

- flatpak
- fzf
- yay

## Installation

Move the script to a directory in your PATH variable.

## Usage

The interface is composed of:
- A package manager to install, remove, and reinstall packages. You can also view details of that package and whether it is installed (and updatable if on AUR).
- A command selector to update your system.
The interface supports multi-selection.
