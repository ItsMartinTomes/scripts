# File Finder & VIM Opener

## Overview

This script provides an interactive way to search for files within a specified directory (default: current directory) using the `fd` command, select one with `fzf` (fuzzy finder), preview its contents with `bat`, and open the selected file in `vim`.

> **Note:** Running this script in large directories (e.g., `$HOME`) may be slow unless you configure `fd` to ignore unnecessary files via `$HOME/.config/fd/ignore`.

---

## Features

- Fast file searching with [`fd`](https://github.com/sharkdp/fd)
- Interactive file selection with [`fzf`](https://github.com/junegunn/fzf)
- File preview with [`bat`](https://github.com/sharkdp/bat)
- Opens the selected file in [`vim`](https://www.vim.org/)

---

## Requirements

Make sure the following tools are installed and available in your `PATH`:

- `vim`
- `fd`
- `fzf`
- `bat`

---

## Usage

`ff [DIRECTORY]`

- If no directory is specified, the script searches in the current directory.

### Example

`ff`
`ff /path/to/project`


---

## How It Works

1. **Search**: Uses `fd` to list files in the specified directory.
2. **Fuzzy Select**: Pipes the file list to `fzf` for interactive selection.
3. **Preview**: Shows file previews using `bat` within `fzf`.
4. **Edit**: Opens the selected file in `vim`.

---

## Configuration

- The script uses the ignore file for `fd` at `$HOME/.config/fd/ignore` to speed up searches in large directories.
- No other configuration is required.

---

## Limitations

- Only works with files (not directories).
- Assumes all dependencies are installed and available in the system's `PATH`.
- Performance in large directories depends on your `fd` ignore configuration.

---
