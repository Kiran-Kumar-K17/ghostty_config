# Terminal Configuration

Personal Linux terminal configuration using **Ghostty**, **Gruvbox Material Dark**, and **JetBrains Mono**.

## Features

* Ghostty terminal
* Gruvbox Material Dark theme
* JetBrains Mono font
* 14px font size
* 95% background opacity
* Custom window padding
* Gruvbox-inspired color overrides
* Minimal Bash prompt

## Ghostty Configuration

Configuration file:

```text
~/.config/ghostty/config
```

### Configuration

```ini
theme = Gruvbox Material Dark

# Font Setup (Uses Fedora's system font + Ghostty's built-in icons)
font-family = JetBrains Mono
font-size = 14

# Window Styles
background-opacity = 0.95
window-padding-x = 10
window-padding-y = 10

# Color Overrides (Matches Gruvbox Theme palette)
background = #282828
foreground = #ebdbb2
cursor-color = #ebdbb2
```

## Bash Prompt

The shell prompt uses a simple colored format:

```bash
PS1="\[\e[38;5;214m\]\u@\h \[\e[38;5;108m\]\w \[\e[38;5;46m\]➜ \[\e[0m\]"
```

It displays:

```text
username@hostname ~/current/directory ➜
```

### Bash Configuration

Add the following to `~/.bashrc`:

```bash
export TERMINAL=ghostty

PS1="\[\e[38;5;214m\]\u@\h \[\e[38;5;108m\]\w \[\e[38;5;46m\]➜ \[\e[0m\]"
```

Reload the configuration:

```bash
source ~/.bashrc
```
