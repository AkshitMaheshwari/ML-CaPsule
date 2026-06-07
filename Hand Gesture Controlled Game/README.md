# 🖐️ Hand Gesture Joystick Control

Control any game using your hand gestures via webcam — no controller needed!  
Uses **MediaPipe** for hand tracking and **PyAutoGUI** to simulate arrow key presses.

---

## 📸 How It Works

Tracks your **wrist point** using MediaPipe. When you show your hand, it auto-calibrates that position as the neutral point. Moving away from it triggers a key press.

```
Hand moves RIGHT  →  Right Arrow Key
Hand moves LEFT   →  Left Arrow Key
Hand moves UP     →  Up Arrow Key
Hand moves DOWN   →  Down Arrow Key
```

---

## 🛠️ Requirements

- Python 3.7 – 3.12
- Webcam

```bash
pip install opencv-python mediapipe pyautogui
```

---

## 🎮 Play a Game

You can play directly while running the notebook!  
Open this alongside your notebook and control it with your hand:

👉 [Subway Surfers on Poki](https://poki.com/en/g/subway-surfers)

---

## 🚀 How to Run

Open `hand_gesture_control.ipynb` in Jupyter and run cells one by one:
1. Install dependencies
2. Import libraries
3. Initialize MediaPipe & Camera
4. Run the main loop

---

## 🎮 Controls

| Key | Action |
|-----|--------|
| Show hand to camera | Auto-calibrates neutral position |
| `c` | Recalibrate |
| `q` | Quit |

---

## ⚙️ Configuration

| Variable | Default | Description |
|----------|---------|-------------|
| `gesture_delay` | `0.5` sec | Time between gesture triggers |
| `dead_zone` | `50` px | How far hand must move to trigger |
| `VideoCapture(1)` | `1` | Camera index — change to `0` if needed |

---

## 🔍 Troubleshooting

| Problem | Fix |
|---------|-----|
| `No module named 'mediapipe'` | Use Python 3.10 or 3.11, not 3.13 |
| `WinError 5 Access is denied` | Run `pip install mediapipe --user` |
| Camera not opening | Change `VideoCapture(1)` to `VideoCapture(0)` |
| Gestures not triggering | Reduce `dead_zone` to 30 |

---

## 📁 Project Structure

```
hand_gesture_controlled_game/
├── hand_gesture_control.ipynb
└── README.md
```

---

## 🧠 Tech Stack

| Library | Purpose |
|---------|---------|
| `OpenCV` | Webcam capture and display |
| `MediaPipe` | Hand landmark detection |
| `PyAutoGUI` | Simulating arrow key presses |

---

Made with ❤️ using Python, OpenCV, and MediaPipe.