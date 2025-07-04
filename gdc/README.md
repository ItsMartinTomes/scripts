
# gdc

A simple shell script to automate `git add` and `git commit` with a timestamped commit message.

---

## Overview

`gdc` is a convenience tool for quickly staging all changes in your current git repository and committing them with a message containing the current date and time. This is useful for fast, descriptive commits during rapid development or for personal projects.

---

## Usage

`gdc`


- Stages all changes (`git add .`)
- Commits with a message formatted as `YYYY-MM-DD HH:MM:SS`

---


---

## How It Works

1. Runs `git add .` to stage all modified, new, and deleted files in the current repository.
2. Runs `git commit -m "<timestamp>"` where `<timestamp>` is the current date and time in the format `YYYY-MM-DD HH:MM:SS`.

---

## Requirements

- [git](https://git-scm.com/) must be installed and available in your `PATH`.
- Must be run inside a git repository.

---

## Notes

- This script does **not** push your changes to a remote repository.
- The commit message will only contain the timestamp.
- Use for quick snapshots or personal workflow; for production or collaborative projects, more descriptive commit messages are recommended.




