
# 🐚 Custom `.zshrc` Configuration

This repository contains a comprehensive and user-friendly `.zshrc` file tailored for interactive `zsh` shells. It improves the user experience through enhanced key bindings, syntax highlighting, prompt customization, history behavior, and more.

---

## 🔧 Features

### Zsh Options
- `autocd`: Change directories without typing `cd`
- `interactivecomments`: Allow inline comments
- `magicequalsubst`: Filename expansion in assignments
- `nonomatch`: Silently ignore unmatched glob patterns
- `notify`: Immediate background job notifications
- `numericglobsort`: Smart numerical sorting
- `promptsubst`: Enable command substitution in prompt

### Prompt Customization
- Supports multiple styles via `PROMPT_ALTERNATIVE` (`twoline`, `oneline`, `backtrack`)
- Dynamically updates prompt appearance
- Terminal title reflects user and path
- Optional newline before prompt

### Key Bindings
- Emacs-style bindings
- Word and line navigation shortcuts
- `Ctrl+P`: Toggle between one-line and two-line prompt

### History Configuration
- Stores history in `~/.zsh_history`
- Ignores duplicate and space-prefixed commands
- Enhanced history expansion behavior

### Completion System
- Auto-descriptions and advanced matching
- Process-aware completion for `kill`
- Menu-based selection with formatting

### Syntax Highlighting
- Uses `zsh-syntax-highlighting` with customized styles
- Highlights commands, arguments, options, etc.

### Auto Suggestions
- Uses `zsh-autosuggestions`
- Configurable suggestion color

### Aliases & Color Support

#### General Command Aliases:
- `ll` → `ls -l`  
  → Long listing format
- `la` → `ls -lA`  
  → Long listing format, including hidden files (except `.` and `..`)
- `l` → `ls -CF`  
  → Compact view with indicators for file types

#### Colored Output:
- `ls` → `ls --color=auto`  
  → Enables color-coded output for files and directories
- `grep` → `grep --color=auto`  
  → Highlights matches in search
- `fgrep` → `fgrep --color=auto`  
  → Literal search with match highlighting
- `egrep` → `egrep --color=auto`  
  → Extended regex search with highlighting
- `ip` → `ip --color=auto`  
  → Colorful output for IP management commands
- `diff` → `diff --color=auto`  
  → Highlights changes in file comparisons

#### Color Schemes:
- If `dircolors` is installed, custom color schemes are applied from `~/.dir_colors` or default settings.

---

## 📁 Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/zshrc-config.git
   ```

2. Backup your current `.zshrc`:
   ```bash
   cp ~/.zshrc ~/.zshrc.backup
   ```

3. Replace it with the custom config:
   ```bash
   cp zshrc-config/.zshrc ~/.zshrc
   ```

4. Reload `zsh`:
   ```bash
   source ~/.zshrc
   ```

---

## 🔄 Prompt Styles

Toggle prompt layout using `Ctrl+P`:
- **twoline** (default): User, host, and path on separate lines
- **oneline**: Compact single-line prompt
- **backtrack**: Colored minimalistic one-liner

Set default style via:

```zsh
PROMPT_ALTERNATIVE=twoline
```

---

## ✅ Dependencies

- [zsh](https://www.zsh.org/)
- [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)
- [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)
- Optional: `dircolors`, `lesspipe`, `command-not-found`, `pipx`

---

## 🧠 Notes

- Designed with Kali Linux in mind but should work cross-distribution.
- Some behavior is conditional based on terminal capability and environment variables.

---

## 📜 License

MIT License. Free to use, modify, and distribute.

---

## ✨ Credits

Heavily inspired by the default Kali Linux `.zshrc` with additional tweaks and enhancements.
