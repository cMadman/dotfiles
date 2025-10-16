# Dotfiles

## Installation

### 1. Install Homebrew

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### 2. Clone this repository

```bash
git clone https://github.com/cMadman/dotfiles.git ~/.config
cd ~/.config
ln -s ~/.config/zshrc ~/.zshrc
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
ln -s ~/.config/Brewfile ~/Brewfile
```

### 6. Install fzf-git.sh

```bash
git clone https://github.com/junegunn/fzf-git.sh.git ~/fzf-git.sh
```

### Safety & Hygiene
Secrets are scrubbed using gitleaks.

To scan for leaks:

```bash
gitleaks detect --source ~/.config
```
