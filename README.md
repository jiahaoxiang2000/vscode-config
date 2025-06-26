# VS Code User Configuration Documentation

This document provides a comprehensive overview of the custom VS Code settings and keybindings configured in this user profile, with a focus on **Vim integration** and enhanced text editing workflows.

## 🎯 Overview

This configuration transforms VS Code into a powerful Vim-centric development environment by combining:

- **Multiple Vim Extensions** (VSCodeVim + Neovim integration)
- **Custom Keybindings** for enhanced navigation
- **Optimized Settings** for Vim workflows
- **Cross-Profile Consistency** for seamless experience

## 📁 File Structure

```
~/.config/Code/User/
├── README.md           # This documentation file
├── settings.json       # Global VS Code settings
├── keybindings.json    # Custom keyboard shortcuts
├── profiles/           # User profiles configuration
└── ...
```

## ⚙️ Settings Overview

### 🛠️ Build Tools

- **Makefile**: Auto-configure on open

### ⌨️ Custom Keybindings

### 🧭 Navigation History (Vim-Compatible)

The keybinding configuration focuses on essential navigation while preserving comprehensive Vim functionality:

| Keybinding | Command          | Description             | Vim Context                         |
| ---------- | ---------------- | ----------------------- | ----------------------------------- |
| `Ctrl+O`   | Navigate Back    | Go to previous location | Matches Vim's `Ctrl+O` jump back    |
| `Ctrl+I`   | Navigate Forward | Go to next location     | Matches Vim's `Ctrl+I` jump forward |

### 🪟 **Vim-Style View Pane Navigation**

Complete Vim-style window and pane management using `Ctrl+W` prefix (traditional Vim pattern):

#### **Editor Group Navigation:**

| Keybinding      | Command                   | Description                    |
| --------------- | ------------------------- | ------------------------------ |
| `Ctrl+W H`      | Focus Previous Group      | Focus left editor group        |
| `Ctrl+W L`      | Focus Next Group          | Focus right editor group       |
| `Ctrl+W J`      | Focus Below Group         | Focus editor group below       |
| `Ctrl+W K`      | Focus Above Group         | Focus editor group above       |
| `Ctrl+W Ctrl+W` | Focus Active Editor Group | Return to editor from any view |

#### **Sidebar & Panel Navigation:**

| Keybinding | Command        | Description               |
| ---------- | -------------- | ------------------------- |
| `Ctrl+W E` | Focus Explorer | Open/focus file explorer  |
| `Ctrl+W G` | Focus Git/SCM  | Focus source control view |

#### **Resize Editor Groups:**

| Keybinding       | Command              | Description          |
| ---------------- | -------------------- | -------------------- |
| `Ctrl+W Shift+H` | Decrease View Width  | Make editor narrower |
| `Ctrl+W Shift+L` | Increase View Width  | Make editor wider    |
| `Ctrl+W Shift+J` | Decrease View Height | Make editor shorter  |
| `Ctrl+W Shift+K` | Increase View Height | Make editor taller   |

#### **Move Editors Between Groups:**

| Keybinding           | Command                       | Description               |
| -------------------- | ----------------------------- | ------------------------- |
| `Ctrl+W Shift+Right` | Move Editor to Next Group     | Move current editor right |
| `Ctrl+W Shift+Left`  | Move Editor to Previous Group | Move current editor left  |

### 🎯 **Essential Vim Commands in VS Code**

#### **Navigation & Movement:**

```vim
" Basic movement
h, j, k, l          " Left, Down, Up, Right
w, b, e             " Word forward, back, end
0, $                " Line start, end
gg, G               " File start, end

" Advanced movement
f{char}, F{char}    " Find character forward/backward
t{char}, T{char}    " To character forward/backward
s{char}{char}       " Sneak: jump to two characters (enabled)
```

#### **Editing Operations:**

```vim
" Text objects
ciw, caw            " Change in/around word
ci", ca"            " Change in/around quotes
ci{, ca{            " Change in/around braces

" Visual selections
v, V, Ctrl+v        " Character, line, block visual mode
gv                  " Reselect last visual selection
```

#### **VS Code Integration:**

```vim
" Command palette
:                   " Opens VS Code command palette

" File operations
:e filename         " Open file
:w                  " Save file
:q                  " Close editor

" Search and replace
/pattern            " Search forward
?pattern            " Search backward
:%s/old/new/g       " Global replace
```

## 📚 Additional Resources with the Plugins on Neovim

Here we integrate the _Neovim on VS Code_ plugin to provide a more Vim-like experience with additional features the more config see [here](https://github.com/jiahaoxiang2000/nvim-config/tree/lazy/lua/vscode-config)
