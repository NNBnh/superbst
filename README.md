<h1 align="center"><i>SuperB ST</i></h1>
<p align="center">ST-base terminal with enough patches</p>
<p align="center"><img src=""></p>
<p align="center"><a href="https://github.com/NNBnh/superbst/blob/main/LICENSE"><img src="https://img.shields.io/badge/license-mit--1.1-%23F7CA88.svg?labelColor=585858&style=for-the-badge&logoColor=FFFFFF" alt="License: MIT"></a> <a href="https://st.suckless.org"><img src="https://img.shields.io/badge/st-0.8.4-%23F7CA88.svg?labelColor=585858&style=for-the-badge&logoColor=FFFFFF" alt="ST 0.8.4"></a></p>
<p align="center"><a href="https://github.com/NNBnh/superbst/watchers"><img src="https://img.shields.io/github/watchers/NNBnh/superbst?labelColor=585858&color=F7CA88&style=flat-square"></a> <a href="https://github.com/NNBnh/superbst/stargazers"><img src="https://img.shields.io/github/stars/NNBnh/superbst?labelColor=585858&color=F7CA88&style=flat-square"></a> <a href="https://github.com/NNBnh/superbst/network/members"><img src="https://img.shields.io/github/forks/NNBnh/superbst?labelColor=585858&color=F7CA88&style=flat-square"></a> <a href="https://github.com/NNBnh/superbst/issues"><img src="https://img.shields.io/github/issues/NNBnh/superbst?labelColor=585858&color=F7CA88&style=flat-square"></a></p>

## 💡 About
**SuperB ST** is a *SuperB* [ST-base](https://st.suckless.org) terminal using [ST-flexipatch](https://github.com/bakkeby/st-flexipatch) to add enough patches so it can be compared with other modern terminal like [Alacritty](https://github.com/alacritty/alacritty) and [Kitty](https://sw.kovidgoyal.net/kitty)

<p align="center"><a href="https://github.com/NNBnh/superb-st/releases"><img src="https://img.shields.io/github/downloads/NNBnh/superb-st/total?color=F7CA88&labelColor=585858&style=for-the-badge&logoColor=FFFFFF" alt="Downloads"></a></p>

### ✨ Features
- **Goal**:
  - Patch features that only the terminal can do
- **Non goal**:
  - Patch features that conflict with the terminal multiplexer or some windows manager's features
  - Patch features that can be integrate using other tools/programs

### 🩹 Patches
- Window:
  - [`anysize`](https://st.suckless.org/patches/anysize): allows the terminal to resize to any pixel size and centers the content of the terminal
  - [`relativeborder`](https://st.suckless.org/patches/relativeborder): allows users to specify a border that is relative in size to the width of a cell in the terminal
  - [`themed_cursor`](https://st.suckless.org/patches/themed_cursor): use the xterm cursor from your cursor theme
  - [`alpha`](https://st.suckless.org/patches/alpha): allows users to only change the opacity of the background (unlike using the composite manager to change the opacity of the whole windows)
- Font:
  - [`wide_glyphs`](https://www.reddit.com/r/suckless/comments/jt90ai/update_support_for_proper_glyph_rendering_in_st): support proper glyph rendering
  - [`ligatures`](https://st.suckless.org/patches/ligatures): support proper ligatures rendering
  - [`boxdraw`](https://st.suckless.org/patches/boxdraw): custom rendering of lines and blocks (but not braille e.g: `⠞⠓⠊⠎`) characters for gapless alignment
- Drawing:
  - [`bold-is-not-bright`](https://st.suckless.org/patches/bold-is-not-bright): makes bold text rendered simply as bold, leaving the color unaffected
  - [`sync`](https://st.suckless.org/patches/sync): better draw timing to reduce flicker/tearing and improve animation smoothness
  - [`w3m`](https://st.suckless.org/patches/w3m): support w3m images hack
- Escape sequences:
  - [`osc_10_11_12_2`](https://st.suckless.org/patches/osc_10_11_12_2): to modify the background, foreground and cursor colors
  - [`blinking_cursor`](https://st.suckless.org/patches/blinking_cursor): to modify cursor style
  - [`undercurl`](https://st.suckless.org/patches/undercurl): to render special underlines
- Beginner friendly:
  - [`scrollback`](https://st.suckless.org/patches/scrollback): scroll back through terminal output using mouse wheel
  - [`clipboard`](https://st.suckless.org/patches/clipboard): support clipboard copy and paste
  - [`xresources`](https://st.suckless.org/patches/xresources): adds the ability to configure ST via [Xresources](https://wiki.archlinux.org/title/X_resources)

## 🚀 Setup
### 🧾 Dependencies
- [`fontconfig`](https://archlinux.org/packages/extra/x86_64/fontconfig) and [`libx11`](https://archlinux.org/packages/extra/x86_64/libx11) are make dependencies
- [`libxft-bgra`](https://aur.archlinux.org/packages/libxft-bgra) is make dependencies for color emoji support

### 📥 Installation
#### 🔧 Manually
Run the following commands:

```sh
git clone https://github.com/NNBnh/superb-st
cd superb-st

git submodule update --init --recursive
git pull origin $(git branch-name)

mkdir -p st
bsymlink st-flexipatch st
ln -sf patches.h config.h config.mk st/

cd st
sudo make install
```

#### 📦 Package manager
For [`nix`](https://nixos.org) user:

```sh
#TODO
```

> *If you can and want to port SuperB ST to other package managers, feel free to do so.*

## ⚙️ Configuration


## 💌 Credits
Special thanks to:
- [**ST**](https://st.suckless.org) by [`suckless.org`](https://suckless.org)
- [ST-flexipatch](https://github.com/bakkeby/st-flexipatch) by [Stein Gunnar Bakkeby](https://github.com/bakkeby)

<br><br><br><br>

---

> <h1 align="center">Made with ❤️ by <a href="https://github.com/NNBnh"><i>NNB</i></a></h1>
>
> <p align="center"><a href="https://www.buymeacoffee.com/nnbnh"><img src="https://img.shields.io/badge/buy_me_a_coffee%20-%23F7CA88.svg?logo=buy-me-a-coffee&logoColor=333333&style=for-the-badge" alt="Buy Me a Coffee"></a></p>
