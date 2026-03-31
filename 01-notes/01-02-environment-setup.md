# 🧪 01-01 Environment Setup

---

## 🐍 Install Python 3

### Option 1: Manual

### Step 1: Go to official Python website: https://www.python.org/downloads/

### Step 2: Download the latest version of Python 

![install-python](image.png)

👉 Download:
- Python 3.x.x (recommended)
O,R
- Python Install Manager (optional)

Step 3: Install Python

IMPORTANT:
✔ Check "Add Python to PATH" before clicking Install

---

### Option 2: PowerShell (Windows)

powershell
### Step 1: Search available Python versions
winget search Python

### Step 2: Install using exact version from search result
winget install Python.Python.<version>

---

✅ Verify Installation
python --version

If not working:

py --version

---

📚 Install Libraries: Command at powershell/terminal

General command: pip install <library_name>

Examples:

pip install numpy           # for ?
pip install pandas          # for ?
pip install matplotlib      # for ?

Optional (for RL):

pip install gymnasium       # for 

---

💻 Install VS Code

Download: https://code.visualstudio.com/

During installation:
✔ Add to PATH
✔ Add "Open with Code"

---

🔌 Install Python Extension

Open VS Code → Extensions → Search: Python

Install: Python (by Microsoft)

NOTE: Python extension does NOT install Python

---