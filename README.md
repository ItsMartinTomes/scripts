# scripts
Set of useful scripts for system administration

## Overview

Use `setup` shell script to create symbolic links for a set of custom scripts into a target directory, making them easily accessible from your command line.

By default, the symlinks are created in `$HOME/.local/bin`, but you can specify a different target directory as an argument.

---

## Usage

`./setup [target_directory]`


- `target_directory` *(optional)*: The directory where symlinks will be created.  
  Defaults to `$HOME/.local/bin` if not provided.

### Examples

- Create symlinks in the default directory:

`./setup /usr/local/bin`


---

## What It Does

- Creates the target directory if it does not exist.
- Executes the `chmod +x` permissions o nthe scripts.
- Creates or updates symbolic links for the following scripts:

- `ff/ff`
- `fs/fs`
- `gdc/gdc`
- `gf/gf`
- `gpt/gpt`
- `pie/pie`
- `rf/rf`

- Symlinks use absolute paths to ensure they work regardless of the current working directory.

---

## Requirements

- The script assumes it is run from the root directory containing the script folders (`ff`, `fs`, `gdc`, etc.).
- You must have execute permissions for the script (`chmod +x setup.sh`).
---

## Notes

- Using `$HOME/.local/bin` as the default target directory follows common Linux user conventions for local executables.
- Make sure your target directory is included in your `PATH` environment variable to run the linked scripts directly.



