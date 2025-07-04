# gpt

A shell script wrapper for [charmbracelet/mods](https://github.com/charmbracelet/mods), designed to streamline usage with OpenAI API key management and user-friendly status text.

---

## Overview

`gpt` is a convenience script for running the [`mods`](https://github.com/charmbracelet/mods) AI-powered command-line tool. It automatically sets your `OPENAI_API_KEY` from a local config file, checks for the presence of `mods`, and provides a custom status text for your AI queries.

---

## Features

- Automatically sets the `OPENAI_API_KEY` environment variable from `$HOME/.config/gpt/token`.
- Checks that `mods` is installed before running.
- Passes all arguments directly to `mods`.
- Sets a custom status text ("Ummm") for your mods session.

---

## Usage

`gpt [arguments]`

All arguments are passed directly to `mods`.

### Example

`gpt "Summarize this text:...."`

---

## How It Works

1. **Checks for `mods`:**  
   The script verifies that the `mods` command is available in your `PATH`. If not, it prints an error and exits.

2. **Loads API Key:**  
   Reads the first line of `$HOME/.config/gpt/token` and sets it as the `OPENAI_API_KEY` environment variable for the session.

3. **Runs mods:**  
   Executes `mods` with the custom status text and any arguments you provide.

---

## Requirements

- [`mods`](https://github.com/charmbracelet/mods) must be installed and in your `PATH`.
- An OpenAI API key saved in `$HOME/.config/gpt/token` (the first line of the file).
- A POSIX-compliant shell.

---

## Notes

- If `mods` is not installed, the script will print `requires charmbracelet/mods` and exit.
- The script is adapted from [rwxrob](https://github.com/rwxrob) and can be customized further as needed.

