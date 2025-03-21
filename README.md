# Starship Dracula Theme 🚀

A **beautiful, modern, and stylish Starship prompt** using the **Dracula color scheme** with **Powerline separators, glyphs, and more**.

## ✨ Features
- 🎨 Dracula Color Palette – Fully themed with Dracula’s dark aesthetics.
- 📂 Stylish Directory Display – Wrapped in 【brackets】 for a clean look.
- 🚀 Custom Prompt Symbol
- 🕒 Time Display
- 📏 Spacing Improvement – Adds a new line before the prompt for better readability.
- 🌱 Git Integration – Displays the current branch and status.
- 🐍 Python Version – Shows the active Python version.
- 📦 Node.js Version – Shows the active Node.js version.
- 🦀 Rust Version – Displays Rust version when in a Rust project.
- 🐳 Docker Context – Shows active Docker environment.

![image](https://github.com/user-attachments/assets/69d720e3-d60c-45a7-9b91-b6f1a017248b)
![image](https://github.com/user-attachments/assets/38d37e12-142e-4a46-ac4f-f2bf88f8ecdd)
![image](https://github.com/user-attachments/assets/2186bd22-637a-4e20-a15e-598ca81f48a2)


<br>

## 📦 Installation Guide
### **1️⃣ Install Dracula theme**
Follow the instructions to download and install the Dracula Theme for [Konsole (Linux)](https://draculatheme.com/konsole), [iTerm (macOS)](https://draculatheme.com/iterm), [PowerShell (Windows)](https://draculatheme.com/powershell), or search for your preferred terminal at [draculatheme.com](https://draculatheme.com).

### **2️⃣ Install [Starship](https://starship.rs/) cross-shell prompt**
- Global:
```bash
curl -sS https://starship.rs/install.sh | sh
```

- Homebrew (macOS):
```bash
brew install starship
```

- Powershell (Windows)
```bash
Invoke-Expression (&starship init powershell)
```

- Ubuntu
```bash
sudo snap install --edge starship
echo 'export STARSHIP_CONFIG="$HOME/snap/starship/common/starship.toml"' >> ~/.zshrc
```

### **3️⃣ Install a Nerd Font**
To display icons properly, install a Nerd Font from [nerdfonts.com](https://nerdfonts.com), such as FiraCode Nerd Font, then set your terminal to use the newly installed font.

- For Linux (Ubuntu, Debian, Arch, Fedora, Kali, and most distros), install FiraCode Nerd Font with:
```bash
mkdir -p ~/.local/share/fonts && cd ~/.local/share/fonts && wget -O FiraCode.zip https://github.com/ryanoasis/nerd-fonts/releases/latest/download/FiraCode.zip && unzip -o FiraCode.zip -d FiraCode && rm FiraCode.zip && fc-cache -fv

```
- For macOS, use Homebrew:
```bash
brew install --cask font-fira-code-nerd-font
```

### **4️⃣ Apply my custom Starship Dracula Theme**
- You can manually copy my starship.toml configuration to ~/.config/starship.toml or download it via:
```bash
mkdir -p ~/.config && curl -fsSL https://raw.githubusercontent.com/Century300/custom-starship-dracula-theme/main/starship.toml -o ~/.config/starship.toml
```

- Occasionally, especially on macOS, Starship may fail to automatically add the required initialization line to `~/.zshrc`. If your prompt does not reflect the Starship theme, you may need to manually add the following line at the bottom of `~/.zshrc`:
```bash
# starship theme https://starship.rs/
eval "$(starship init zsh)"
```
- If you install Starship via Snap in Ubuntu, move the config file to: $HOME/snap/starship/common/starship.toml.

- To apply changes, restart your shell by 'exec zsh' or 'source ~/.zshrc' or both.

<br>

## Other notes
- **📂 Folder Path Display (Truncation):**
By default, this theme displays the full folder path unless it becomes too long.
If you prefer a shorter path, you can change truncation_length to 3 to only display the last 3 folders:
```toml
# Stylish Directory
[directory]
format = "(purple)【📂[$path]($style)】(purple)"
style = "bold purple"
truncation_length = 20
truncation_symbol = "…/"
```

- **Zsh (Z shell) vs Bash (Bourne Again Shell):**
This setup is intended for Zsh. If you prefer Bash, simply replace .zshrc with .bashrc in the instructions above.
If you're not sure which shell you're using, run 'echo $SHELL' in your terminal.

- **Colors:**
Some colors from the Dracula palette are defined but not currently used — this is intentional, to make it easier for others to customize or extend this theme with consistent style.
