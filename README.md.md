# Sentinel-Edge-Core

**Sentinel-Edge-Core** is an autonomous industrial Edge AI kernel designed for high-performance, offline-first safety operations. It provides real-time LiDAR data processing, anomaly detection, and safety-critical state management for industrial robotics.

---

## 🚀 Project Overview
This project is engineered to operate entirely at the edge on industrial hardware (such as **NVIDIA Jetson**). It eliminates the need for cloud connectivity, ensuring data sovereignty and ultra-low latency response times for safety-critical environments.

## ⚙️ Key Technical Pillars
* **Zero-Cloud Sovereignty:** Full operational autonomy with no external network dependency.
* **Integrity Guard:** Self-verifying codebase using **SHA-256 signatures** to prevent unauthorized tampering or modifications.
* **Statistical Anomaly Detection:** Real-time **Z-score analysis** over a sliding window to detect subtle sensor irregularities.
* **Fault-Tolerant Runtime:** Automated recovery mechanisms with exponential back-off strategies to ensure continuous uptime.

## 🗺️ Safety Zones Configuration
The system categorizes sensor inputs into four distinct safety zones:

| Zone | Distance | Action |
| :--- | :--- | :--- |
| **CRITICAL** | < 0.8m | Emergency Stop (Hard Stop) |
| **WARNING** | 0.8m – 1.5m | Alert + Automated Slow-down |
| **CAUTION** | 1.5m – 3.0m | Logging + System Monitoring |
| **SAFE** | > 3.0m | Normal Operation |

## 🛠️ Deployment

### Prerequisites
* Python 3.8+
* Linux-based Industrial Edge Controller or NVIDIA Jetson device.

### Quick Start
1. **Clone the repository:**
   ```bash
   git clone [https://github.com/your-username/sentinel-edge-core.git](https://github.com/your-username/sentinel-edge-core.git)
   Execute the kernel:

Bash
python sentinel_kernel.py
📋 System Outputs
sentinel.log: Full runtime operation logs.

sentinel.hash: Security baseline (SHA-256).

sentinel_health.json: Live system health reporting (JSON).

anomaly_log.json: Detailed logs of detected statistical anomalies.

👤 Author
Soufiane Hajou Industrial Maintenance & Edge AI Specialist

Built for Industry 4.0 | Privacy-First Robotics
