# Dracula Starship Theme 🚀

A **beautiful, modern, and stylish Starship prompt** using the **Dracula color scheme** with **Powerline separators, glyphs, and enhanced Git integration**.

## ✨ Features
- 🎨 **Dracula Color Palette** for a stunning dark mode experience.
- 🚀 **Custom prompt symbols** for a modern feel.
- 📂 **Powerline separators** for directory and Git branch.
- 🌱 **Git integration** (branch + status).
- 🐍 **Python & 📦 Node.js version display**.
- ✅ **Works out of the box with Starship & Nerd Fonts**.

## 📦 Installation Guide

### **1️⃣ Install [Starship](https://starship.rs/) cross-shell prompt**
```bash
curl -sS https://starship.rs/install.sh | sh
```
Homebrew (macOS):
```bash
brew install starship
```
Powershell (Windows)
```bash
Invoke-Expression (&starship init powershell)
```

### **2️⃣ Install a Nerd Font
To display icons properly, install a Nerd Font from https://www.nerdfonts.com/, such as FiraCode Nerd Font, then change your terminal font manually:
```bash
mkdir -p ~/.local/share/fonts && cd ~/.local/share/fonts && wget -O FiraCode.zip https://github.com/ryanoasis/nerd-fonts/releases/latest/download/FiraCode.zip && unzip -o FiraCode.zip -d FiraCode && rm FiraCode.zip && fc-cache -fv
```

### **3️⃣ Apply my custom Starship Dracula Theme**
I borrowed the  color coding and added new codes.
You can copy my starship.toml codes manually to ~/.config/starship.toml or download my codes via:

I used the color coding from the [Dracula Starship GitHub
](https://github.com/dracula/starship/blob/9f2c60b5e6de26e340d8d91ba6c4a725e56d6992/starship.toml) and added my own configurations. You can manually copy my starship.toml source code to ~/.config/starship.toml or download it via:
```bash
mkdir -p ~/.config && curl -fsSL https://raw.githubusercontent.com/Century300/custom-starship-dracula-theme/main/starship.toml -o ~/.config/starship.toml
```

Apply changes:
```bash
exec zsh
```

### 📂 Folder Path Display (Truncation)
By default, this theme displays the full folder path in most cases.
However, if the path contains more than 20 folders, it will be truncated, showing only the last 20 folders.
If you prefer a shorter path, you can change truncation_length to 3 to only display the last 3 folders:
```toml
[directory]
format = "[](purple)📂 [$path]($style)[](purple) "
style = "bold purple"
truncation_length = 20
truncation_symbol = "…/"
```





