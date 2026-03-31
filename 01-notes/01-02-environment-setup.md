# 🧪 01-01 Environment Setup

---

## 🐍 Install Python 3

### Option 1: Manual

1. Download:
https://www.python.org/downloads/

2. Install Python

IMPORTANT:
✔ Check "Add Python to PATH"

---

### Option 2: PowerShell (Windows)

```powershell
winget install Python.Python.3

Verify Installation
python --version

If not working:

py --version
💻 Install VS Code

Download:
https://code.visualstudio.com/

During installation:
✔ Add to PATH
✔ Add "Open with Code"

🔌 Install Python Extension

Open VS Code → Extensions → Search:

Python

Install:

Python (by Microsoft)

NOTE:
Python extension does NOT install Python

📚 Install Libraries
pip install numpy pandas matplotlib

Optional (RL):

pip install gymnasium