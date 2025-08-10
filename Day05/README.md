# Villain Framework - Installation Guide (Linux)

Villain is a Command & Control (C2) framework for managing reverse shells and remote access payloads.  
This guide covers installation on Linux in one go.

---

## 1. Requirements

Before installing Villain, ensure you have the following dependencies:

- Python 3.10 or newer
- `git`
- `pip` (Python package manager)
- `virtualenv` (optional but recommended)
- `nmap` (optional but useful for network tasks)

Install them using:

```bash
sudo apt update && sudo apt install -y python3 python3-pip python3-venv git nmap
```

---

## 2. Clone the Repository

```bash
git clone https://github.com/t3l3machus/Villain.git
cd Villain
```

---

## 3. (Optional) Create a Virtual Environment

It’s recommended to keep dependencies isolated:

```bash
python3 -m venv venv
source venv/bin/activate
```

---

## 4. Install Dependencies

```bash
pip install --upgrade pip
pip install -r requirements.txt
```

If you face permission issues, use:

```bash
pip install --user -r requirements.txt
```

---

## 5. Run Villain

```bash
python3 villain.py
```

If you’re in a virtual environment, simply run:

```bash
./villain.py
```

---

## 6. Notes

- Use Villain only on systems you have permission to test.
- For persistent usage, create an alias in your `.bashrc` or `.zshrc`:
  
```bash
alias villain='cd /path/to/Villain && python3 villain.py'
```

- If you get a `ModuleNotFoundError`, re-run:
  
```bash
pip install -r requirements.txt
```

---

## 7. Troubleshooting

- **Python not found**: Install Python 3 with `sudo apt install python3`.
- **Permission denied**: Use `chmod +x villain.py` before running.
- **Dependency errors**: Ensure `pip` is upgraded (`pip install --upgrade pip`).

---

## 8. Uninstall / Remove Villain

To remove Villain completely:

```bash
rm -rf Villain
```

If you created a virtual environment, deactivate and remove it:

```bash
deactivate
rm -rf venv
```

---

### ⚠ Disclaimer
This tool is for educational and authorized security testing purposes **only**.  
Misuse of Villain for unauthorized access is illegal and punishable by law.
