# Remove Files

## rf - Remove Files

`rf` is a Perl script that deletes files containing a specified string in their filenames. It supports recursive deletion in subdirectories.

### Motivation
After using and paying for [Proton Drive](https://proton.me/drive) for a year, I suddenly found nearly all my files (>10k) duplicated with strange `(# Name Clash` in their names, doubling my storage usage. 

I opened a support ticket, but they told me to delete all the files manually! I replied that they have no moral right to make me delete tens of thousands of files due to their error and asked for a script to remove the duplicates. They refused. 

So, I made my own and am sharing it publicly. 

### Requirements

- Perl 5.40.1 or later (with `threads` and `threads::shared` modules, included in core Perl)

###  Installation

1. Save the script as `rf`.
2. Make it executable:
   ```sh
   chmod +x rf
   ```
3. Place it in a directory in your `$PATH` (e.g., `/usr/local/bin`).

### Usage

```sh
rf "string" [-r] [DIRECTORY]
```

#### Options

- `-h`, `--help`: Show help message and exit
- `-r`: Recursively delete files in subdirectories (uses threads)

#### Arguments
- `"string"`: String to match in filenames (required, in double quotes)
- `DIRECTORY`: Directory to search (optional, defaults to current directory)

### Examples

Delete files in the current directory:
```sh
./rf "Name Clash"
```
Delete files recursively in the current directory:
```sh
./rf "2025" -r
```
Delete files in a specific directory recursively:
```sh
./rf "(# Name Clash" /path/to/dir -r
```
Show help:
```sh
./rf -h
```

### Features
- Deletes files matching a specified string in their names.
- Detailed output showing checked files, matches, and deletions.
- Error checking for directory access and file deletion.

### Notes
- The search string must be enclosed in quotes (single or double) due to shell argument parsing.

