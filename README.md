# Face Catcher

Face Catcher is a webcam-controlled arcade game. Move your head to line up with falling orbs and stars, then open your mouth to catch them. Dodge bombs and build your combo. During a boss fight, pinch a bomb with your thumb and index finger and drag it onto the boss.

## Run on Windows

You'll need Python 3.12 and a webcam. In PowerShell, run these commands:

```powershell
git clone https://github.com/knarfbv/face-catcher.git
cd face-catcher
py -3.12 -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
.\.venv\Scripts\python.exe facecatcher.py
```

If you already cloned the repository, start with the virtual environment command from inside the project folder. If the webcam fails to open, check Windows camera permissions and close any app using it. If you have multiple cameras, change `CAM_SOURCE` in `facecatcher.py` from `0` to the device index you want to use.

## Controls

| Key | Action |
| --- | --- |
| Space | Start, restart, pause, or resume |
| M | Toggle the face mesh |
| C | Cycle the HUD color theme |
| S | Save a screenshot to the current folder |
| F | Refocus the game window |
| Esc | Return to the main menu |
| Q | Quit |

The game processes webcam frames locally. Screenshots are saved as `capture_*.png` and ignored by Git, along with the virtual environment.
