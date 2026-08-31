# BoxForge

```bash
┌────────────────────────────────────────────────────────────────────────┐
│  ____   ___  __  __ _____ ___  ____   ____ _____                       │
│ | __ ) / _ \ \ \/ /|  ___/ _ \|  _ \ / ___| ____|                      │
│ |  _ \| | | | \  / | |_ | | | | |_) | |  _|  _|                        │
│ | |_) | |_| | /  \ |  _|| |_| |  _ <| |_| | |___                       │
│ |____/ \___/_/_/\_\|_|   \___/|_| \_\\____|_____|  v4.8.0              │
│     [Unified Multi-Backend Package Manager & Zero-Trust Core]          │
└────────────────────────────────────────────────────────────────────────┘
```

**BoxForge** is a unified package management utility for **GNU Operating System / H-Linux** that 
provides a consistent command-line interface for managing packages across multiple ecosystems, 
complete with zero-trust local integrity signing and verification.

---

## Requirements

-   `GNU Operating System / H-Linux`
-   `H-Linux human command layer`
-   `H-Linux env library`
-   `NLP`
-   `nlp-bin`
-   `nlp-aur-bin`

---

## Features

-   Unified CLI
-   Native NLP backend (`nlp-bin`)
-   AUR support (`nlp-aur-bin`)
-   Integrated `.dsigned` SHA-256 package signing + verification architecture
-   Local package gatekeeping and installation verification
-   `Flatpak` support
-   `Snap` support
-   Unified Update tool `update-all` (experimental)

---

## Getting BoxForge

```bash
> gh repo clone https://www.github.com/fpucore/boxforge.git

> goto boxforge
```

### Staging:

```bash
> newdir "$HOME/.hwm"

> copy boxforge "$HOME/.hwm/"

> make-executable "$HOME/.hwm/boxforge"
```

### Installing (with ScriptForge):

```bash
> scriptforge

[ScriptForge] Enter the full path to the directory containing the script(s) (e.g., /home/user/scripts):
~/.hwm/boxforge
```

### Verify the installation:

```bash
> boxforge --version
```

---

## Usage

```bash
Usage:
  boxforge <prompt> [pkg]

Prompts:
  install [pkg]           Install NLP package
  install-local [file]    Verify .dsigned signature and install local NLP package
  remove [pkg]            Remove NLP package
  update                  Update NLP packages (with .dsigned integrity checks)
  search <query>          Search NLP repositories
  search-local <query>    Search installed NLP packages
  list                    List installed NLP packages
  info [pkg]              Show NLP package info

  sign <file>             Generate a .dsigned SHA-256 signature for a package
  verify <file>           Verify a package against its .dsigned file
  clean-cache             Clean orphaned .dsigned files from package caches

  install-aur [pkg]       Install AUR package
  update-aur              Update AUR packages
  search-aur <query>      Search AUR

  install-flatpak [pkg]   Install Flatpak package
  remove-flatpak [pkg]    Remove Flatpak package
  update-flatpak          Update Flatpak packages
  search-flatpak <query>  Search Flatpak
  info-flatpak [pkg]      Show Flatpak package info
  list-flatpak            List installed Flatpak packages

  install-snap [pkg]      Install Snap package
  remove-snap [pkg]       Remove Snap package
  update-snap             Update Snap packages
  search-snap <query>     Search Snap
  info-snap [pkg]         Show Snap package info
  list-snap               List installed Snap packages

  update-all              (1)Execute the Unified Update tool

  version, --version      Show BoxForge version
  help, --help            Show this help

  ---
  Note (1): The Unified Update tool is currently implemented as an experimental feature of BoxForge.
  Execution of this tool can be network and resource intensive, and in some cases may require manual
  user intervention. If you are not confident with manual intervention of updating packages then
  just use the regular update procedures.
  ---
```

---

## Considered or Planned Features

-   Unified search
-   Backend detection
-   Modular function
-   BXF package archive support
-   ~~Cryptographic package signing~~ ✅ Done

---

## License

This project is licensed under the **MIT License**. See the `LICENSE` file for details.

---

## Author

Chris McGimpsey-Jones (2026) <chrisjones.unixmen@gmail.com>
