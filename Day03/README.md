
# 💻 Install Visual Studio Code on Kali Linux (VirtualBox)

This guide explains how to **update Kali Linux to the latest version** and then **download and install Visual Studio Code**, all while running Kali inside **VirtualBox**.

---

## 🛠️ Step 1: Update Kali Linux to the Latest Version

To ensure smooth installation and compatibility, start by updating your system.

### 🔧 Commands to Run:

```bash
sudo apt update && sudo apt upgrade -y
```

> This updates all installed packages to their latest versions.

### 🔄 Reboot (if required):

```bash
sudo reboot
```

---

## 📦 Step 2: Download and Install Visual Studio Code

Visual Studio Code is not available in the default Kali repo, so you need to install it manually.

### 📥 Download the `.deb` Installer

#### Option 1: Download via Browser
- Go to: [https://code.visualstudio.com/download](https://code.visualstudio.com/download)
- Select `.deb` under **Linux** download options

#### Option 2: Download via Terminal
```bash
wget https://code.visualstudio.com/sha/download?build=stable&os=linux-deb-x64 -O vscode.deb
```

---

### 📦 Install the `.deb` File

Use the `dpkg` command to install the downloaded package:

```bash
sudo dpkg -i vscode.deb
```

> If you encounter missing dependencies, run the following command:

```bash
sudo apt --fix-broken install
```

Then, reinstall:
```bash
sudo dpkg -i vscode.deb
```

---

## 🚀 Step 3: Launch Visual Studio Code

After successful installation, launch VS Code using:

```bash
code
```

> If the command is not recognized, try restarting the terminal or rebooting the system.

---

## 🧩 Optional: Install Useful VS Code Extensions

Once VS Code is open:
- Go to the **Extensions** panel (square icon on the sidebar)
- Search and install extensions like:
  - Python
  - C/C++
  - Live Server
  - GitLens

---

## 🐞 Troubleshooting

| Issue                                    | Solution                                             |
|-----------------------------------------|------------------------------------------------------|
| VS Code doesn't launch                  | Run `sudo apt --fix-broken install` and reinstall   |
| `code` command not found                | Log out and log back in or reboot system            |
| Network error during download           | Ensure your VM has network access enabled           |

---

## 📚 Useful Commands Summary

| Command                         | Purpose                               |
|----------------------------------|----------------------------------------|
| `sudo apt update`               | Refresh package list                   |
| `sudo apt upgrade -y`           | Install updates                        |
| `sudo dpkg -i vscode.deb`       | Install downloaded VS Code `.deb` file |
| `sudo apt --fix-broken install` | Fix broken or missing dependencies     |
| `code`                          | Launch Visual Studio Code              |

---

## ✅ You're Done!

You’ve successfully:
- Updated your Kali Linux system
- Installed Visual Studio Code
- Set up a development environment inside VirtualBox

Happy coding!

---

**Author:** Tenzin Rigzin  
**Platform:** Kali Linux (VirtualBox)  
**Last Updated:** July 2025
