# fs

A powerful, interactive file search and navigation tool for your terminal.

## Overview

`fs` lets you search for text patterns in files within a directory using [ripgrep (rg)](https://github.com/BurntSushi/ripgrep), interactively filter results with [fzf](https://github.com/junegunn/fzf), preview file contents with [bat](https://github.com/sharkdp/bat), and jump directly to a line in [neovim (nvim)](https://neovim.io/).

---

## Features

- Fast text search with ripgrep
- Fuzzy, interactive result filtering with fzf
- File previews with bat, highlighting the matching line
- Open selected file at the matching line in neovim

---

## Usage

`fs [directory] [search term]`


- If **both arguments** are provided:  
  `fs <directory> <search term>`  
  Searches for `<search term>` in the specified `<directory>`.

- If **only one argument** is provided and it is a directory:  
  `fs <directory>`  
  Shows all files in the directory (not very useful without a search term).

- If **only one argument** is provided and it is **not** a directory:  
  `fs <search term>`  
  Searches for `<search term>` in the current directory.

### Examples

`fs . "main"`
`fs src "function"`
`fs "TODO"`


---

## Dependencies

- [ripgrep (rg)](https://github.com/BurntSushi/ripgrep)
- [fzf](https://github.com/junegunn/fzf)
- [bat](https://github.com/sharkdp/bat)
- [neovim (nvim)](https://neovim.io/) (can be replaced with vim if you modify the script)

Make sure all dependencies are installed and available in your `PATH`.

---

## How It Works

1. **Search**: Uses `rg` to search for the given term in the specified directory.
2. **Filter**: Pipes the results to `fzf` for interactive narrowing.
3. **Preview**: Uses `bat` to preview the file, highlighting the matching line.
4. **Edit**: Pressing `Enter` opens the selected file at the matching line in `nvim`.

---

## Customization

- To use `vim` instead of `nvim`, change the last line of the script.

