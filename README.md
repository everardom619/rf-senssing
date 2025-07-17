# 📡 RF Sensing Project

A hands-on project for exploring the **core concepts of RF data processing** using a Software Defined Radio (SDR). This project captures, processes, and visualizes real-time RF spectrum data to detect signals based on configurable thresholds.

---

## 🧠 Purpose

This project is designed to help learners and developers understand:

- SDR configuration and data acquisition
- Signal processing fundamentals (FFT, windowing, power spectrum)
- Real-time signal detection
- Visualization of RF spectrum data

---

## 📁 Project Structure

```
rf_sensing_project/
│
├── rf_sensing/                  # Main package
│   ├── __init__.py
│   ├── config.py                # Configuration constants
│   ├── sdr_interface.py         # SDR setup and teardown
│   ├── signal_processing.py     # Signal processing and detection logic
│   └── visualization.py         # Plotting and display logic
│
├── main.py                      # Entry point for the application
├── requirements.txt             # Dependencies
└── README.md                    # Project overview and usage
```

---

## ⚙️ Configuration (`config.py`)

Key parameters for SDR and signal detection:

```python
SDR_IP = "ip:192.168.2.1"
CENTER_FREQ = 2450e6
SAMPLE_RATE = 5e6
RX_LO = int(CENTER_FREQ)
RX_BUFFER_SIZE = 4 * 1024
GAIN_CONTROL_MODE = "slow_attack"
RX_GAIN_DB = 70
DETECTION_THRESHOLD_DB = -25
```

---

## 🚀 How to Run

### 1. Install Dependencies

```bash
pip install -r requirements.txt
```

### 2. Connect Your SDR

Ensure your **ADI Pluto SDR** is connected and accessible at the configured IP address.

### 3. Run the Application

```bash
python main.py
```

Press `Ctrl+C` to stop the application.

---

## 📊 What You’ll See

- A real-time plot of the RF spectrum
- Signal detection status based on a configurable threshold
- Visual feedback when a signal is detected

---

## 🧩 Core Modules

- **`sdr_interface.py`**: Initializes and tears down the SDR connection.
- **`signal_processing.py`**: Applies FFT and detects signals based on power threshold.
- **`visualization.py`**: Displays the spectrum and detection status in real time.

---

## 🛠️ Requirements

- Python 3.x
- ADI Pluto SDR
- Python packages:
  - `numpy`
  - `matplotlib`
  - `adi` (Analog Devices' SDR interface)

---

## 📚 Learning Goals

- Understand how to interface with SDR hardware
- Learn basic RF signal processing techniques
- Visualize and interpret RF spectrum data
- Build a foundation for more advanced RF sensing applications
