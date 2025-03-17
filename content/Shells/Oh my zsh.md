Oh My Zsh (OMZ) is a powerful framework for managing the Zsh shell configuration. It provides themes, plugins, and extensive customization options.

---

## Installation

### Prerequisites
- Install Zsh:
  ```bash
  sudo apt install zsh   # Debian-based
  sudo dnf install zsh   # Fedora-based
  sudo pacman -S zsh     # Arch-based
  ```
- Verify installation:
  ```bash
  zsh --version
  ```

### Install Oh My Zsh
- Via curl:
  ```bash
  sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
  ```
- Via wget:
  ```bash
  sh -c "$(wget https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"
  ```
- Switch to Zsh:
  ```bash
  chsh -s $(which zsh)
  ```

---

## Configuration

### Changing Themes
- Themes are located in `~/.oh-my-zsh/themes/`
- Set theme in `~/.zshrc`:
  ```bash
  ZSH_THEME="agnoster"
  ```
- Apply changes:
  ```bash
  source ~/.zshrc
  ```

### Popular Themes
- `robbyrussell` (default, minimal Git integration)
- `agnoster` (powerline style, needs Powerline fonts)
- `powerlevel10k` (highly customizable, fastest prompt)

### Powerline Fonts (for some themes)
```bash
git clone https://github.com/powerline/fonts.git --depth=1
cd fonts && ./install.sh && cd .. && rm -rf fonts
```

---

## Plugins

### Enabling Plugins
- Modify `~/.zshrc`:
  ```bash
  plugins=(git zsh-autosuggestions zsh-syntax-highlighting)
  ```
- Apply changes:
  ```bash
  source ~/.zshrc
  ```

### Popular Plugins
- `git` (Git shortcuts)
- `zsh-autosuggestions` (suggest commands as you type)
- `zsh-syntax-highlighting` (syntax colorization)
- `docker` (Docker command aliases)
- `vi-mode` (Vim-like editing in the shell)

---

## Customization

### Aliases
Define in `~/.zshrc`:
```bash
alias ll='ls -la'
alias gs='git status'
```

### Functions
```bash
mkcd() {
    mkdir -p "$1" && cd "$1"
}
```

---

## Updating & Uninstalling

### Update Oh My Zsh
```bash
omz update
```

### Uninstall Oh My Zsh
```bash
uninstall_oh_my_zsh
```

---

## Troubleshooting

### Theme Not Changing?
```bash
exec zsh
```

### Plugin Not Working?
- Ensure it's listed in `plugins=()`
- Run:
  ```bash
  source ~/.zshrc
  
