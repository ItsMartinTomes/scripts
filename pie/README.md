# pie

A simple shell script for in-place string replacement in files using Perl.

---

## Overview

`pie` (Perl In-place Edit) is a command-line utility that performs global search-and-replace operations on a specified file. It uses Perl's powerful regular expression engine to safely and efficiently replace all occurrences of a search string with a replacement string, modifying the file in place.

---

## Usage

`pie search_string replace_string filename`


- `search_string`: The string to search for in the file.
- `replace_string`: The string to replace each occurrence of `search_string`.
- `filename`: The file in which to perform the replacement.

**Example:**

`pie foo bar myfile.txt`

This command replaces all occurrences of `foo` with `bar` in `myfile.txt`.

---

## How It Works

1. Checks that exactly three arguments are provided.
2. Uses Perl's in-place editing mode (`-pi`) to perform a global (`g`) substitution:
    - `\Q` and `\E` are used to escape any special characters in the search string, ensuring a literal match.
3. The specified file is modified directly.

---

## Requirements

- [Perl](https://www.perl.org/) must be installed and available in your `PATH`.

---

## Notes

- The replacement is **global** (all occurrences in each line will be replaced).
- The script does not create a backup of the file. Consider making a manual backup if needed.
- Special characters in the search string are automatically escaped for safety.
- This script is intended for simple literal replacements. For more advanced regex, modify the Perl command as needed.
