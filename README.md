# QUANTUM VISION X 

## Overview

**Quantum Vision X** is an intelligent CCTV intrusion detection system designed for real-time perimeter and area security. It continuously monitors CCTV/RTSP camera feeds, detects unauthorized intrusions using computer vision, and triggers alerts and backend updates instantly. The system is optimized for multi-camera environments and supports scalable deployment for campuses, offices, warehouses, and restricted zones.

---

## Key Capabilities

* Real-time intrusion detection from CCTV / IP camera feeds
* Supports multiple RTSP cameras simultaneously (multi-threaded)
* Motion and object-based intrusion analysis
* Day/Night robust detection using frame preprocessing
* Automatic alert triggering and backend updates
* Centralized monitoring with camera-wise status tracking
* Designed for continuous 24×7 surveillance

---

## System Architecture

Quantum Vision X processes live CCTV feeds, performs frame analysis, detects intrusions, and updates the system state via database/API integration.

**High-level flow:**

```
CCTV / IP Camera (RTSP)
        ↓
Frame Capture (OpenCV)
        ↓
Preprocessing (Grayscale, Noise Reduction)
        ↓
Intrusion Detection Logic
        ↓
Alert Generation & Status Update
        ↓
Backend / Database
```

---

## Project Structure

```
data/
├── models/                     # Pre-trained detection models
├── camera_config/              # Camera IP & RTSP configurations
├── logs/                       # System logs

intrusion_detection.py          # Core intrusion detection logic
camera_monitor.py               # Multi-camera monitoring & threading
alert_manager.py                # Alert and notification handling
status_updater.py               # Backend & database updates
main.py                         # System entry point
```

---

## How It Works

### 1. Camera Monitoring

* Each CCTV camera is accessed via RTSP.
* Camera connectivity is verified continuously.
* Each camera runs in a dedicated thread for parallel processing.

### 2. Frame Processing

* Frames are captured in real time.
* Converted to grayscale for faster processing.
* Noise reduction and normalization applied.

### 3. Intrusion Detection

* Motion and object presence are analyzed.
* Threshold-based and model-based logic determines intrusion.
* Distinguishes normal background activity from unauthorized movement.

### 4. Alert & Status Update

* Intrusion events are logged immediately.
* Camera-wise intrusion status is updated.
* Backend API / database receives real-time updates.

---

## Detection Logic (Conceptual)

* Continuous frame comparison
* Brightness and motion intensity analysis
* Region-of-interest based intrusion validation
* False-positive reduction using temporal consistency

---

## Multi-Camera Support

* Thread-based architecture
* Thread-safe shared status storage
* Independent failure handling per camera
* Scales easily with additional cameras

---

## Use Cases

* Office and corporate security
* Industrial area surveillance
* Campus and hostel monitoring
* Restricted zone protection
* Warehouse and storage facilities

---

## Requirements

* Python 3.x
* OpenCV
* NumPy
* Requests
* Threading support

---

## Installation

Install required dependencies:

```bash
pip install opencv-python numpy requests
```

Configure camera RTSP URLs in the camera configuration file before running the system.

---

## Running the System

```bash
python main.py
```

The system will:

* Initialize all CCTV cameras
* Start real-time monitoring
* Detect intrusions
* Update alerts automatically

---

## Advantages of Quantum Vision X

* Real-time intrusion detection
* Low latency processing
* Scalable multi-camera architecture
* Automated backend integration
* Reduced manual monitoring effort

---

## Confidentiality Notice

This repository contains **documentation and architectural details only**. Core implementation files are excluded due to confidentiality and security agreements.

---

**Quantum Vision X** – Intelligent Surveillance. Proactive Security.
