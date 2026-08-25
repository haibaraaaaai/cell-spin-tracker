# CellSpinTracker

CellSpinTracker is a small analysis toolkit for tethered-cell videos.
It focuses on rotation frequency and CW/CCW direction detection from microscopy movies.

## Project Status

This project is currently paused (maintenance-only).

- The original active development period has ended.
- Code remains in the repository for reproducibility and later follow-up experiments.
- Planned revisit: when new experimental runs are available and the setup is verified.

If you return to this project later, start by re-validating the full analysis pipeline on a small, known video set before batch processing.

## Current Scientific Context

Recent context from team emails and archived material indicates:

- Martin's 2022 videos include a small number of clear switching cells (reported: 6 cells among many spinners, likely a few percent at most, depending on selection bias).
- Leah's report describes a larger CCW fraction under high load (CW bias around 0.68) but no direct switching seen over the observation window.
- An upcoming goal is to determine whether new experiments reproduce Martin-like behavior (rare switchers) or Leah-like behavior (larger CCW fraction without visible switching).

Practical next analysis goals when work resumes:

1. Quantify switching-cell fraction automatically from video batches.
2. Compare across conditions and loads (especially tethered high-load conditions).
3. Re-test attractant removal conditions to increase or control switching frequency.

## Installation

Install required packages:

```sh
pip install numpy opencv-python matplotlib
```

Clone repository:

```sh
git clone https://github.com/haibaraaaaai/CellSpinTracker.git
cd CellSpinTracker
```

## Usage

Run:

```sh
python main.py
```

Then select an AVI file in the dialog. Output files are written next to the input video unless changed in code.

## Repository Layout

- main.py: entry point
- preprocessing.py: image preprocessing helpers
- circle_detection.py: bead/cell circular feature detection
- roi_extraction.py: region-of-interest extraction
- calculate_frequency.py: frequency and direction calculations
- data/: local data artifacts (do not commit large raw datasets)

## Author

Daping Xu
daping.xu@physics.ox.ac.uk
