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

| Keybinding | Command          | Description               |
| ---------- | ---------------- | ------------------------- |
| `Ctrl+W E` | Focus Explorer   | Open/focus file explorer  |
| `Ctrl+W G` | Focus Git/SCM    | Focus source control view |
| `Ctrl+W D` | Focus Debug      | Focus debug view          |
| `Ctrl+W X` | Focus Extensions | Focus extensions view     |
| `Ctrl+W P` | Focus Problems   | Focus problems panel      |

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

#### **Editor Management:**

| Keybinding       | Command                  | Description                |
| ---------------- | ------------------------ | -------------------------- |
| `Ctrl+W S`       | Split Editor Down        | Split current editor down  |
| `Ctrl+W V`       | Split Editor Right       | Split current editor right |
| `Ctrl+W Q`       | Close Active Editor      | Close current editor       |
| `Ctrl+W Shift+Q` | Close Other Editors      | Close all other editors    |
| `Ctrl+W N`       | Next Editor in Group     | Switch to next editor tab  |
| `Ctrl+W Shift+N` | Previous Editor in Group | Switch to previous editor  |

#### **Chat Interface Navigation:**

| Keybinding | Command          | Description                        |
| ---------- | ---------------- | ---------------------------------- |
| `J`        | Scroll Down (6x) | Scroll down in chat history (fast) |
| `K`        | Scroll Up (6x)   | Scroll up in chat history (fast)   |
| `Tab`      | Toggle Focus     | Switch between input and history   |

#### **Neovim Treewalker Integration:**

| Keybinding     | Command               | Description                |
| -------------- | --------------------- | -------------------------- |
| `Ctrl+Shift+K` | Treewalker Swap Up    | Swap with element above    |
| `Ctrl+Shift+J` | Treewalker Swap Down  | Swap with element below    |
| `Ctrl+Shift+H` | Treewalker Swap Left  | Swap with element to left  |
| `Ctrl+Shift+L` | Treewalker Swap Right | Swap with element to right |

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

## 🔧 Neovim Integration

### vscode-neovim Configuration

This setup uses the `vscode-neovim` extension for a more authentic Vim experience:

- **Clean Mode**: Disabled (`neovimClean: false`) for full Neovim features
- **Control Key Passthrough**: Extensive Ctrl key mappings for both insert and normal modes
- **Extension Affinity**: Isolated to worker process 1 for optimal performance
- **Composite Keys**: Ready for custom escape sequences (currently disabled)

### Control Key Mappings

**Insert Mode**: `a`, `d`, `h`, `j`, `m`, `o`, `r`, `t`, `u`, `w`
**Normal Mode**: `a`, `d`, `f`, `h`, `i`, `j`, `k`, `l`, `m`, `o`, `r`, `t`, `u`, `v`, `n`, `x`, `/`, `]`

### Profile-Based Configuration

Settings are configured to apply across all VS Code profiles, ensuring consistent behavior:

- Core Neovim settings synchronized across profiles
- Editor preferences maintained globally
- Keybinding consistency across different workspace types

## 📚 Additional Resources

For advanced Neovim configuration examples, see the [nvim-config repository](https://github.com/jiahaoxiang2000/nvim-config/tree/lazy/lua/vscode-config)
