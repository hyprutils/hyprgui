<div align='center'>

<h2>HyprGUI <img src='https://raw.githubusercontent.com/hyprutils/.github/refs/heads/main/hyprutils.png'width='18' height='18'></h2>

<img src='.github/hyprgui.png' width='200' height='200'>

An unofficial GUI for configuring Hyprland, built with GTK4 and Rust. 🚀🦀<br>
Comes with a custom hyprparser for Hyprland's configuration file. (Rust btw) 🦀

## Preview
![Preview](.github/preview.png)

</div>

## Installation

[![Packaging status](https://repology.org/badge/vertical-allrepos/hyprgui.svg)](https://repology.org/project/hyprgui/versions)

### GitHub Releases
See HyprGUI's [releases page](https://github.com/hyprutils/hyprgui/releases) for downloadable binaries.

### Arch Linux
There are 2 different [AUR](https://aur.archlinux.org) packages available:

- [hyprgui](https://aur.archlinux.org/packages/hyprgui) - Latest release built from source
- [hyprgui-bin](https://aur.archlinux.org/packages/hyprgui-bin) - Latest release in binary form

Install the preferred package with:
```bash
git clone https://aur.archlinux.org/<package>.git
cd <package>
makepkg -si
```

Or, if you're using an [AUR Helper](https://wiki.archlinux.org/title/AUR_helpers), it's even simpler (using [paru](https://github.com/Morganamilo/paru) as an example):
```bash
paru -S <package>
```

### Nix
You can install HyprGUI with Nix in three ways:

#### NixOS Configuration
Add the following Nix code to your NixOS Configuration, usually located in `/etc/nixos/configuration.nix`
```nix
environment.systemPackages = [
  pkgs.hyprgui
];
```

#### nix-env
On NixOS:
```bash
nix-env -iA nixos.hyprgui
```

On Non NixOS:
```bash
# without flakes:
nix-env -iA nixpkgs.hyprgui
# with flakes:
nix profile install nixpkgs#hyprgui
```

#### nix-shell
```bash
nix-shell -p hyprgui
```

## Building from source
1. Install Rust (preferably `rustup`) through your distro's package or [the official script](https://www.rust-lang.org/tools/install)
2. Install `git`, `pango` and `gtk4`
3. Clone this repository:
`git clone https://github.com/hyprutils/hyprgui && cd hyprgui`
4. Compile the app with `cargo build --release` or run it directly with `cargo run --release`

## TODO:
- [x] Implement GUI
- [x] Implement parser
- [x] Improve the readme
- [ ] Improve parser
- [ ] Improve GUI

## Credits:
- [Vaxry](https://github.com/vaxerski) - Hyprland
- [rust-gtk](https://github.com/gtk-rs/gtk4-rs) - The GTK4 library
- [Hyprland](https://github.com/hyprwm/Hyprland) - The wayland compositor

<h6 align='center'>Copyright (C) 2026 HyprUtils<h6>
