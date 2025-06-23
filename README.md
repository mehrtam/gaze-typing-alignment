Gaze-Typing Alignment Analysis
This project analyzes human gaze and typing behavior by aligning timestamped keystroke events with normalized gaze coordinates. The goal is to study gaze-key distance, typing attention, and spatial correlation during text entry.

What's Inside
Typing event extraction from JSON logs (textInput events)

Gaze point filtering and normalization from Tobii-style .txt logs

Timestamp alignment using interpolation (±50ms tolerance)

Gaze–key distance computation

Correlation analysis between gaze and typing positions

Time-series visualization of X/Y alignment

Requirements
Python ≥ 3.7

Libraries: pandas, numpy, matplotlib

To install the dependencies:

bash
Copy
Edit
pip install pandas numpy matplotlib
Input Files
Place the following files in the root of your Colab or local project:

File	Description
One participant .json file	Typing logs with textInput events
One participant .txt file	Gaze logs (Tobii-style JSON per line format)

Note: You may use the Eye of the Typer (EOTT) dataset as a substitute for the original files.

Output & Metrics
Plots of Typing vs. Gaze (X and Y over time)

Gaze–key Euclidean distance

Correlation coefficients for X and Y alignment

Use Cases
Human-Computer Interaction (HCI)

Assistive typing or AR/VR experiments

Cognitive load and attention studies

Eye-tracking behavior analysis

Sample Result
Typing vs Gaze X alignment over time

![image](https://github.com/user-attachments/assets/51e6a196-aae2-4cc3-b009-fcdc54ac2ecd)


Notes
Gaze values are assumed to be normalized (0–1) and mapped to screen dimensions.

Gaze filtering removes out-of-bound or corrupted data points.

Data privacy is respected — no personally identifiable content is shared.

Author
Fateme Eslami

AI MSc | University of Birmingham

Gaze-aware AI Systems for Typing Interfaces

