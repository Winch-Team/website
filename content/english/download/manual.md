---
title: "Manual Installation"
draft: false
---

<span style="color:#DE3163">This method is <strong style="color:red">not recommended</strong> as it can lead to unexpected installation</span>. Use this as a last way to install winch; we will not provide any help with this method.


1. **Open Terminal:**
   - Launch your terminal application.

2. **Check for Sudo Access:**
   - Ensure you have sudo access. You may need to enter your password when prompted.

3. **Create Installation Directory:**
   - Run the following command to create the directory where Winch will be installed:
     ```bash
     mkdir -p "$HOME/.winch/bin"
     ```

5. **Download the Winch Binary:**
   - **For Linux:**
     - Run the following command to download the Linux binary:
       ```bash
       curl -fsSL https://github.com/Winch-Team/winch/releases/download/v0.1.0/winch-gnu-linux-x86_64 -o "$HOME/.winch/bin/winch"
       ```
   - **For macOS:**
     - Run the following command to download the macOS binary:
       ```bash
       curl -fsSL https://github.com/Winch-Team/winch/releases/download/v0.1.0/winch-macos-x86_64 -o "$HOME/.winch/bin/winch"
       ```

6. **Make the Binary Executable:**
   - Change the permissions to make the Winch binary executable:
     ```bash
     chmod +x "$HOME/.winch/bin/winch"
     ```

7. **Add Winch to Your PATH:**
   - To make Winch accessible from the terminal, add the following line to your shell profile (`~/.bashrc` for Bash or `~/.zshrc` for Zsh):
     ```bash
     export PATH=$PATH:$HOME/.winch/bin/
     ```

8. **Restart Your Shell:**
   - Close and reopen your terminal

9. **Verify Installation:**
   - Run the following command to verify that Winch is installed correctly:
     ```bash
     winch --version
     ```

### Note:
- Ensure that you have internet access during this installation process as the script downloads binaries from GitHub.
- If you encounter any issues, please check your internet connection or the URLs provided in the commands.