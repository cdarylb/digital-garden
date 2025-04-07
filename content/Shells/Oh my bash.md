
**Oh My Bash (OMB)** is a framework that enhances the Bash shell experience by adding themes, plugins, and convenient aliases. It is inspired by Oh My Zsh and is particularly useful for those who prefer Bash but want an improved user experience.

---

## Installation

### Prerequisites

Verify Bash version with:

```bash
bash --version
```

If necessary, install Bash:

```bash
sudo apt install bash   # Debian-based systems
sudo dnf install bash   # Fedora-based systems
sudo pacman -S bash     # Arch-based systems
```

### Installing Oh My Bash

To install Oh My Bash, run the following command:

```bash
bash -c "$(curl -fsSL https://raw.githubusercontent.com/ohmybash/oh-my-bash/master/tools/install.sh)"
```

or using `wget`:

```bash
bash -c "$(wget https://raw.githubusercontent.com/ohmybash/oh-my-bash/master/tools/install.sh -O -)"
```

After installation, restart the shell:

```bash
exec bash
```

---

## Configuration

### Changing Themes

Oh My Bash comes with multiple themes located in `~/.oh-my-bash/themes/`.

```bash
ls ~/.oh-my-bash/themes/
```

To change the theme, edit the `~/.bashrc` file:

```bash
vi ~/.bashrc
```

Locate the line:

```bash
OSH_THEME="font"
```

Replace `font`, e.g., `agnoster`, `powerline`, etc. Save and apply changes:

```bash
source ~/.bashrc
```

### Popular Themes

Some commonly used themes:

- **agnoster**: Minimalist, this is the theme I use
- **powerline**: Inspired by Powerline, requires Powerline fonts
- **simple**: Lightweight, no distractions
- **dst**: Shows useful Git information

To preview themes, check [Oh My Bash Theme Gallery](https://github.com/ohmybash/oh-my-bash/wiki/Themes).

#### Powerline Fonts Installation (Optional)

For `powerline` or `agnoster`, need to install Powerline fonts:

```bash
git clone https://github.com/powerline/fonts.git --depth=1
cd fonts
./install.sh
cd .. && rm -rf fonts
```

Update terminal settings to use a Powerline-compatible font.

---


### Enabling Plugins

To enable plugins, edit `~/.bashrc`:

```bash
vi ~/.bashrc
```

Find the `OSH_PLUGINS` line and modify it:

```bash
OSH_PLUGINS=(git python alias-finder extract)
```

Apply the changes:

```bash
source ~/.bashrc
```

### Popular Plugins

- **git**: Adds useful Git aliases
- **python**: Simplifies Python virtual environment handling
- **alias-finder**: Helps locate available aliases
- **extract**: Extracts compressed files using `x` command

List all available plugins:

```bash
ls ~/.oh-my-bash/plugins/
```

---

## Customizing Aliases & Functions

### Adding Aliases

Define custom aliases in `~/.bashrc`:

```bash
alias ll='ls -alF'
alias gs='git status'
```

Apply changes:

```bash
source ~/.bashrc
```

### Custom Functions

Define functions for repetitive tasks:

```bash
function mkcd() {
    mkdir -p "$1" && cd "$1"
}
```

---

## Updating & Uninstalling Oh My Bash

### Updating Oh My Bash

To update to the latest version:

```bash
git -C ~/.oh-my-bash pull
```

### Uninstalling Oh My Bash

To remove Oh My Bash:

```bash
bash ~/.oh-my-bash/tools/uninstall.sh
```

Restore the sad default Bash settings:

```bash
source ~/.bashrc
```

---

## Troubleshooting

### Issue: Theme Not Changing

Try restarting the shell:

```bash
exec bash
```

Ensure the theme name is correct and exists in `~/.oh-my-bash/themes/`.

### Issue: Plugin Not Working

Make sure the plugin is correctly added in `OSH_PLUGINS` and that sourced `.bashrc`:

```bash
source ~/.bashrc
```

---