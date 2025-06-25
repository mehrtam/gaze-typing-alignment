# Gaze-Typing Alignment & Fixation Analysis

This project analyzes human gaze and typing behavior by aligning timestamped keystroke events with eye-tracking data. It focuses on **where and when users look** during typing, using **fixation detection**, **gaze–key distance**, and **time-aligned visualizations**.

---

## 🎯 What's Inside

- ✅ Typing event extraction from JSON logs (`textInput` events)
- ✅ Gaze point filtering and normalization from Tobii-style `.txt` logs
- ✅ **Fixation detection** using a sliding time window + standard deviation threshold
- ✅ Timestamp alignment of gaze and typing via interpolation (±50ms tolerance)
- ✅ **Fixation-to-keystroke alignment**: How early people look before pressing a key
- ✅ Gaze–key **Euclidean distance** computation
- ✅ Lag analysis (how many milliseconds gaze precedes typing)
- ✅ Pearson **correlation analysis** between fixation positions and typed key positions
- ✅ **Time-series plots** of gaze vs typed X/Y
- ✅ **Fixation heatmaps** and keyboard overlays

---

## 📦 Requirements

- Python ≥ 3.7

### Install dependencies:
```bash
pip install pandas numpy matplotlib seaborn
📁 Input Files
Place the following files in your working directory (Colab or local):

File	Description
P_XX.json	Typing logs with textInput events
P_XX.txt	Gaze logs (Tobii-style JSON-per-line)

👉 You may use the Eye of the Typer (EOTT) dataset as a sample source.

📈 Output & Metrics
📊 Correlation coefficients (X and Y) between fixation and typed keys

⌛ Fixation lag (time between fixation and keypress)

📏 Fixation-to-key distance (in pixels)

🧠 Fixation summary: duration, location, and frequency

🔥 Heatmap of all fixations before typing

⌨️ Keyboard overlay with fixation points and typed characters

🧠 Use Cases
Human-Computer Interaction (HCI)

Assistive typing interfaces (e.g., for disabilities)

AR/VR gaze-based input systems

Cognitive attention studies

Predictive gaze-aware keyboards

🖼️ Sample Visuals
Typing vs Gaze X Alignment

Fixation Heatmap

Keyboard + Fixation Overlay

⚙️ Fixation Detection Parameters
You can adjust:

window_duration: duration of sliding window (e.g., 200–300 ms)

std_threshold: gaze position standard deviation threshold (e.g., 35 px)

These impact how strict the fixation detection is.

👤 Author
Fateme Eslami
MSc Artificial Intelligence, University of Birmingham
Research focus: Gaze-aware AI Systems for Typing Interfaces

🔐 Notes
Gaze data is assumed to be normalized (0–1) and mapped to screen resolution.

All gaze and keystroke timestamps are in milliseconds.

