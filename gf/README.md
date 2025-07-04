# gf

A shell script to format Go source files using `gofmt` and `goimports`, designed for use from the standard Unix editor `ed`.

---

## Overview

`ed-gofmt` is a helper script that formats a Go source file in place by running both `gofmt` and `goimports` on it. It is intended to be called from within `ed` (the standard Unix line editor), but can also be used from the command line.

---

## Usage

Just run the `gf %` from within the `ed` editor. 


---

## How It Works

1. Runs `gofmt -w <filename>` to format the Go source file according to Go standards.
2. Runs `goimports -w <filename>` to organize and fix imports in the Go source file.

Both commands modify the file in place.

---

## Requirements

- [gofmt](https://golang.org/cmd/gofmt/) (comes with Go)
- [goimports](https://pkg.go.dev/golang.org/x/tools/cmd/goimports)
- [ed](https://pubs.opengroup.org/onlinepubs/9699919799/utilities/ed.html) (for use within the editor)

All tools must be installed and available in your `PATH`.

---

## Notes

- The script is especially useful when editing Go files with `ed`, but can be used with any editor or from the terminal.
- The file specified as the argument will be modified in place.
