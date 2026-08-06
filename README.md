# BoxForge

**BoxForge** is a package management utility for **GNU Operating System / H-Linux** that
provides a consistent command-line interface for managing packages across multiple ecosystems.

---

## Requirements

-   `GNU Operating System / H-Linux instance`
-   `H-Linux human command layer`
-   `H-Linux env library`
-   `NLP`
-   `nlp-bin`
-   `nlp-aur-bin`

---

## Features

-   Unified CLI
-   NLP backend (`nlp-bin`)
-   AUR support (`nlp-aur-bin`)
-   `Flatpak` support
-   `Snap` support
-   Unified Update tool `update-all` (experimental)

---

## Getting BoxForge

```bash
> gh repo clone https://www.github.com/fpucore/boxforge.git

> goto boxforge
```

### Installing

```bash
> newdir "$HOME/.hwm"

> copy boxforge "$HOME/.hwm/"

> make-executable "$HOME/.hwm/boxforge"
```

### Create prompt:

```bash
> elevate ln -s "$HOME/.hwm/boxforge" /usr/bin/boxforge
```

### Verify the installation:

```bash
> boxforge --version
```

---

## Usage

```bash
  install <pkg>           Install a package
  remove <pkg>            Remove a package
  update                  Update the system
  search <query>          Search repositories
  search-local <query>    Search installed packages
  list                    List installed packages
  info <pkg>              Show package info

  install-aur <pkg>       Install AUR package
  update-aur              Update AUR packages
  search-aur <query>      Search AUR

  install-flatpak <pkg>   Install Flatpak package
  remove-flatpak <pkg>    Remove Flatpak package
  update-flatpak          Update Flatpak packages
  search-flatpak <query>  Search Flatpak
  info-flatpak <pkg>      Show Flatpak package info
  list-flatpak            List installed Flatpak packages

  install-snap <pkg>      Install Snap package
  remove-snap <pkg>       Remove Snap package
  update-snap             Update Snap packages
  search-snap <query>     Search Snap
  info-snap <pkg>         Show Snap package info
  list-snap               List installed Snap packages

  update-all              (1)Execute the Unified Update tool (experimental)

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
-   Cryptographic package signing

---

## License

This project is licensed under the **MIT License**. See the `LICENSE` file for details.

---

## Author

Chris McGimpsey-Jones (2026) <chrisjones.unixmen@gmail.com>
