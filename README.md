# Zack Reed’s Dotfiles

A curated setup for macOS featuring Aerospace, Sketchybar, Ghostty, and Zsh — all version-controlled and 1Password-secure.

## What's Included

- [x] macOS tiling via **Aerospace**
- [x] Custom status bar via **Sketchybar**
- [x] Terminal: **Ghostty**
- [x] Secure SSH/Git signing via **1Password CLI**
- [x] Zsh with autosuggestions, syntax highlighting, and aliases
- [x] Brewfile to install everything in one command

---

## 🧰 Installation

### 1. Install Homebrew

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### 2. Clone this repository

```bash
git clone https://github.com/rubylaser/dotfiles.git ~/dotfiles
cd ~/dotfiles
```

### 3. Install all apps with the Brewfile

```bash
brew bundle --file=Brewfile
```

### 4. Set Zsh as your default shell (if not already)

```bash
chsh -s /bin/zsh
```

### 5. Link the config files

```bash
ln -s ~/dotfiles/.zshrc ~/.zshrc
ln -s ~/dotfiles/Brewfile ~/Brewfile
```

You can also symlink the full .config folder if this repo is ~/.config.

### 1Password Setup
Make sure you’ve installed 1Password and are signed in:

```bash
eval $(op signin)
export SSH_AUTH_SOCK="$HOME/Library/Group Containers/2BUA8C4S2C.com.1password/t/agent.sock"
```

### Safety & Hygiene
Secrets are scrubbed using gitleaks.

To scan for leaks:

```bash
gitleaks detect --source ~/.config
```