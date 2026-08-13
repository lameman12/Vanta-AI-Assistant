# Manual Installation Guide - Vanta

This includes the requirements, installation steps and troubleshooting when downloading Vanta.

## Requirements

* Windows 10 or Windows 11
* 64-bit Windows
* Internet connection
* Python 3.11
* Vanta Assistant source code

---

## 1. Download Python 3.11

Download the official Python 3.11.9 Windows 64-bit installer:

```text
https://www.python.org/ftp/python/3.11.9/python-3.11.9-amd64.exe
```

Run the downloaded installer.

---

## 2. Install Python 3.11

When the Python installer opens, enable:

```text
Add python.exe to PATH
```

Then click:

```text
Install Now
```

Wait for the installation to finish.

If you see:

```text
Disable path length limit
```

click it.

Then click:

```text
Close
```

---

## 3. Open Command Prompt

Press:

```text
Win + R
```

Type:

```text
cmd
```

Press Enter.

---

## 4. Verify Python 3.11

Run:

```bat
py -3.11 --version
```

You should see:

```text
Python 3.11.9
```

Check the exact Python executable:

```bat
py -3.11 -c "import sys; print(sys.executable)"
```

---

## 5. Upgrade pip

Run:

```bat
py -3.11 -m pip install --upgrade pip
```

Wait for it to finish.

---

## 6. Install All Vanta Dependencies

Run:

```bat
py -3.11 -m pip install --upgrade numpy requests sounddevice faster-whisper pycaw pyautogui pyperclip
```

This installs:

```text
numpy
requests
sounddevice
faster-whisper
pycaw
pyautogui
pyperclip
```

---

## 7. What the Packages Are Used For

### NumPy

Vanta imports:

```python
import numpy as np
```

Package:

```text
numpy
```

Install:

```bat
py -3.11 -m pip install numpy
```

### Requests

Vanta imports:

```python
import requests
```

Package:

```text
requests
```

Install:

```bat
py -3.11 -m pip install requests
```

### SoundDevice

Vanta imports:

```python
import sounddevice as sd
```

Package:

```text
sounddevice
```

Install:

```bat
py -3.11 -m pip install sounddevice
```

### Faster-Whisper

Vanta imports:

```python
from faster_whisper import WhisperModel
```

Package:

```text
faster-whisper
```

Install:

```bat
py -3.11 -m pip install faster-whisper
```

### Pycaw

Vanta imports:

```python
from pycaw.pycaw import AudioUtilities
```

Package:

```text
pycaw
```

Install:

```bat
py -3.11 -m pip install pycaw
```

### PyAutoGUI

Vanta imports:

```python
import pyautogui
```

Package:

```text
pyautogui
```

Install:

```bat
py -3.11 -m pip install pyautogui
```

### Pyperclip

Vanta imports:

```python
import pyperclip
```

Package:

```text
pyperclip
```

Install:

```bat
py -3.11 -m pip install pyperclip
```

---

## 8. Standard Library Imports

The following imports are already included with Python 3.11.

They do not need to be installed with pip:

```text
json
os
queue
difflib
shutil
subprocess
tempfile
threading
random
time
tkinter
tkinter.messagebox
webbrowser
math
winsound
getpass
urllib.request
uuid
pathlib
datetime
```

Do not run commands such as:

```bat
pip install json
pip install os
pip install tkinter
pip install pathlib
```

They are already part of Python.

---

## 9. Verify Every Vanta Import

Run:

```bat
py -3.11 -c "import json, os, queue, difflib, shutil, subprocess, tempfile, threading, random, time, tkinter, tkinter.messagebox, webbrowser, math, winsound, getpass, urllib.request, uuid; from pathlib import Path; from datetime import datetime; import numpy, requests, sounddevice, faster_whisper, pycaw.pycaw, pyautogui, pyperclip; print('ALL VANTA IMPORTS OK')"
```

A successful result is:

```text
ALL VANTA IMPORTS OK
```

---

## 10. Locate the Vanta Source Folder

Find the folder containing:

```text
VantaAssistant.pyw
```

Open Command Prompt.

Use:

```bat
cd "PATH\TO\VANTA"
```

Replace:

```text
PATH\TO\VANTA
```

with the actual folder containing the Vanta source code.

Example:

```bat
cd "C:\Vanta"
```

---

## 11. Check That VantaAssistant.pyw Exists

Run:

```bat
dir VantaAssistant.pyw
```

You should see:

```text
VantaAssistant.pyw
```

If Windows reports:

```text
File Not Found
```

you are in the wrong directory.

Use:

```bat
cd
```

to see the current directory.

Then use:

```bat
cd "PATH\TO\VANTA"
```

to enter the correct directory.

---

## 12. Run Vanta Assistant

Run:

```bat
py -3.11 VantaAssistant.pyw
```

Vanta should start.

Using:

```bat
py -3.11
```

ensures that Python 3.11 is being used.

---

## 13. Check the Exact Python Vanta Uses

Run:

```bat
py -3.11 -c "import sys; print('Python version:', sys.version); print('Python executable:', sys.executable)"
```

The output should show Python 3.11.

---

## 14. Check Installed Packages

Run:

```bat
py -3.11 -m pip list
```

The list should contain:

```text
faster-whisper
numpy
pyautogui
pycaw
pyperclip
requests
sounddevice
```

Package versions may differ.

---

## 15. Check Individual Packages

Check Faster-Whisper:

```bat
py -3.11 -m pip show faster-whisper
```

Check NumPy:

```bat
py -3.11 -m pip show numpy
```

Check SoundDevice:

```bat
py -3.11 -m pip show sounddevice
```

Check Pycaw:

```bat
py -3.11 -m pip show pycaw
```

Check PyAutoGUI:

```bat
py -3.11 -m pip show pyautogui
```

Check Pyperclip:

```bat
py -3.11 -m pip show pyperclip
```

---

## 16. If a Package Is Missing

Install it with:

```bat
py -3.11 -m pip install --upgrade PACKAGE_NAME
```

For example:

```bat
py -3.11 -m pip install --upgrade pyautogui
```

---

## 17. If Python 3.11 Is Not Found

Run:

```bat
py -3.11 --version
```

If it fails, reinstall Python 3.11 using:

```text
https://www.python.org/ftp/python/3.11.9/python-3.11.9-amd64.exe
```

During installation make sure:

```text
Add python.exe to PATH
```

is enabled.

After installation, close Command Prompt.

Open a new Command Prompt and run:

```bat
py -3.11 --version
```

---

## 18. If `python` Shows Python 3.12

If:

```bat
python --version
```

shows Python 3.12, that does not necessarily mean Python 3.11 is unavailable.

Check:

```bat
py -3.11 --version
```

If that shows Python 3.11, use:

```bat
py -3.11
```

for Vanta.

Install packages using:

```bat
py -3.11 -m pip install --upgrade numpy requests sounddevice faster-whisper pycaw pyautogui pyperclip
```

Run Vanta using:

```bat
py -3.11 VantaAssistant.pyw
```

---

## 19. If pip Is Not Recognized

Do not rely on:

```bat
pip install ...
```

Use:

```bat
py -3.11 -m pip install ...
```

For example:

```bat
py -3.11 -m pip install --upgrade numpy requests sounddevice faster-whisper pycaw pyautogui pyperclip
```

---

## 20. Troubleshooting Faster-Whisper

Upgrade Faster-Whisper:

```bat
py -3.11 -m pip install --upgrade faster-whisper
```

Test it:

```bat
py -3.11 -c "from faster_whisper import WhisperModel; print('Faster-Whisper OK')"
```

Expected output:

```text
Faster-Whisper OK
```

---

## 21. Troubleshooting SoundDevice

Reinstall SoundDevice:

```bat
py -3.11 -m pip install --upgrade --force-reinstall sounddevice
```

Test it:

```bat
py -3.11 -c "import sounddevice as sd; print(sd.query_devices())"
```

This should display the available audio devices.

---

## 22. Troubleshooting Pycaw

Reinstall Pycaw:

```bat
py -3.11 -m pip install --upgrade --force-reinstall pycaw
```

Test it:

```bat
py -3.11 -c "from pycaw.pycaw import AudioUtilities; print('Pycaw OK')"
```

Expected output:

```text
Pycaw OK
```

---

## 23. Troubleshooting PyAutoGUI

Reinstall PyAutoGUI:

```bat
py -3.11 -m pip install --upgrade --force-reinstall pyautogui
```

Test it:

```bat
py -3.11 -c "import pyautogui; print('PyAutoGUI OK')"
```

Expected output:

```text
PyAutoGUI OK
```

---

## 24. Troubleshooting Pyperclip

Reinstall Pyperclip:

```bat
py -3.11 -m pip install --upgrade --force-reinstall pyperclip
```

Test it:

```bat
py -3.11 -c "import pyperclip; print('Pyperclip OK')"
```

Expected output:

```text
Pyperclip OK
```

---

## 25. Reinstall All Third-Party Dependencies

If the Python environment becomes corrupted or packages are missing, run:

```bat
py -3.11 -m pip install --upgrade --force-reinstall numpy requests sounddevice faster-whisper pycaw pyautogui pyperclip
```

Then verify:

```bat
py -3.11 -c "import numpy, requests, sounddevice, faster_whisper, pycaw.pycaw, pyautogui, pyperclip; print('ALL THIRD-PARTY PACKAGES OK')"
```

Expected:

```text
ALL THIRD-PARTY PACKAGES OK
```

---

## 26. Complete Environment Verification

Run:

```bat
py -3.11 -c "import json, os, queue, difflib, shutil, subprocess, tempfile, threading, random, time, tkinter, tkinter.messagebox, webbrowser, math, winsound, getpass, urllib.request, uuid; from pathlib import Path; from datetime import datetime; import numpy, requests, sounddevice, faster_whisper, pycaw.pycaw, pyautogui, pyperclip; import sys; print('VANTA ENVIRONMENT READY'); print('Python:', sys.version); print('Executable:', sys.executable)"
```

A successful result should contain:

```text
VANTA ENVIRONMENT READY
Python: 3.11...
Executable: ...
```

---

# PyInstaller

## 27. Install PyInstaller

To create a Windows EXE, install PyInstaller:

```bat
py -3.11 -m pip install --upgrade pyinstaller
```

Check the installed version:

```bat
py -3.11 -m PyInstaller --version
```

---

## 28. Prepare the Vanta Folder

The source folder should contain:

```text
VantaAssistant.pyw
vantaicon.ico
```

Make sure the icon is a valid Windows `.ico` file.

---

## 29. Build a Normal Windowed EXE

Open Command Prompt in the folder containing the source file.

Run:

```bat
py -3.11 -m PyInstaller --clean --noconfirm --onefile --windowed --icon="vantaicon.ico" --name="VantaAssistant" "VantaAssistant.pyw"
```

The normal PyInstaller output will be placed in the `dist` directory.

The executable will be:

```text
dist\VantaAssistant.exe
```

---

## 30. Build the EXE Directly Into the Current Folder

If the executable should be placed directly beside the Python source file, run:

```bat
py -3.11 -m PyInstaller --clean --noconfirm --onefile --windowed --icon="vantaicon.ico" --name="VantaAssistant" --distpath="." "VantaAssistant.pyw"
```

The result will be:

```text
VantaAssistant.exe
```

---

## 31. Remove the Spec File

PyInstaller normally generates a `.spec` file.

If it is not needed, delete it after the build:

```bat
del /q VantaAssistant.spec
```

The EXE itself is unaffected.

---

## 32. Remove Old Build Files

Before rebuilding, you can remove previous PyInstaller output:

```bat
rmdir /s /q build
rmdir /s /q dist
del /q VantaAssistant.spec
```

If a file or folder does not exist, Windows may report an error. That is harmless.

Then rebuild:

```bat
py -3.11 -m PyInstaller --clean --noconfirm --onefile --windowed --icon="vantaicon.ico" --name="VantaAssistant" --distpath="." "VantaAssistant.pyw"
```

---

## 33. Debug an EXE That Immediately Closes

A `--windowed` build does not provide a console window.

For troubleshooting, temporarily create a console-enabled build:

```bat
py -3.11 -m PyInstaller --clean --noconfirm --onefile --console --icon="vantaicon.ico" --name="VantaAssistantDebug" "VantaAssistant.pyw"
```

Run:

```bat
VantaAssistantDebug.exe
```

Any Python exception should appear in the Command Prompt.

After fixing the problem, build the normal version again:

```bat
py -3.11 -m PyInstaller --clean --noconfirm --onefile --windowed --icon="vantaicon.ico" --name="VantaAssistant" --distpath="." "VantaAssistant.pyw"
```

---

# Complete Commands

## Python Check

```bat
py -3.11 --version
```

## Python Location

```bat
py -3.11 -c "import sys; print(sys.executable)"
```

## Upgrade pip

```bat
py -3.11 -m pip install --upgrade pip
```

## Install Vanta Dependencies

```bat
py -3.11 -m pip install --upgrade numpy requests sounddevice faster-whisper pycaw pyautogui pyperclip
```

## Verify Imports

```bat
py -3.11 -c "import json, os, queue, difflib, shutil, subprocess, tempfile, threading, random, time, tkinter, tkinter.messagebox, webbrowser, math, winsound, getpass, urllib.request, uuid; from pathlib import Path; from datetime import datetime; import numpy, requests, sounddevice, faster_whisper, pycaw.pycaw, pyautogui, pyperclip; print('ALL VANTA IMPORTS OK')"
```

## Run Vanta

```bat
py -3.11 VantaAssistant.pyw
```

## Install PyInstaller

```bat
py -3.11 -m pip install --upgrade pyinstaller
```

## Build VantaAssistant.exe

```bat
py -3.11 -m PyInstaller --clean --noconfirm --onefile --windowed --icon="vantaicon.ico" --name="VantaAssistant" --distpath="." "VantaAssistant.pyw"
```

---

# Final Project Structure

After a successful build, the important files can be:

```text
Vanta/
├── VantaAssistant.pyw
├── vantaicon.ico
└── VantaAssistant.exe
```

The `.pyw` file is the Python source.

The `.ico` file is the application icon.

The `.exe` file is the packaged Windows application.

---

# Quick Start

For a fresh Python 3.11 installation:

```bat
py -3.11 -m pip install --upgrade pip
py -3.11 -m pip install --upgrade numpy requests sounddevice faster-whisper pycaw pyautogui pyperclip
py -3.11 -c "import numpy, requests, sounddevice, faster_whisper, pycaw.pycaw, pyautogui, pyperclip; print('ALL VANTA IMPORTS OK')"
```

Run Vanta:

```bat
py -3.11 VantaAssistant.pyw
```

Build the EXE:

```bat
py -3.11 -m pip install --upgrade pyinstaller
py -3.11 -m PyInstaller --clean --noconfirm --onefile --windowed --icon="vantaicon.ico" --name="VantaAssistant" --distpath="." "VantaAssistant.pyw"
```

The final executable is:

```text
VantaAssistant.exe
```
