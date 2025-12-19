# Grid Pattern & Fault Detection using OpenCV

## Overview
This project provides a Python-based computer vision solution for analyzing 8x8 grid patterns (such as chessboards) to identify color anomalies. The script systematically scans the grid, validates the expected background color (Black/White), and identifies specific colored markers placed on "faulty" squares.

## Features
* **Coordinate-Based Sampling:** Uses precise pixel indexing to traverse an 8x8 grid.
* **Automated Logic Validation:** Implements chessboard parity logic to determine whether a cell should be black or white based on its position.
* **Color Classification:** Detects and labels specific BGR markers including Orange, Green, Blue, and Red.
* **Efficient Processing:** Built using NumPy for fast pixel comparison and OpenCV for image handling.

---

## Technical Specifications

### Grid Logic
The detector uses a coordinate system based on a starting offset and a consistent step size between the centers of each square:

* **Start Coordinates:** (105, 105)
* **Step Increment:** 60px
* **Parity Check:** * If $(row + column)$ is **even** $\rightarrow$ Expected: **White**
    * If $(row + column)$ is **odd** $\rightarrow$ Expected: **Black**

### Target Marker Colors
The script identifies the following specific colors if they deviate from the expected background:

| BGR Value | Color Name |
| :--- | :--- |
| `(0, 165, 255)` | Orange |
| `(0, 255, 0)` | Green |
| `(255, 255, 0)` | Blue |
| `(0, 0, 255)` | Red |

---

## Getting Started

### Prerequisites
You will need Python 3.x and the following libraries:
```bash
pip install opencv-python numpy

