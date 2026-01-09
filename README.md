# Groundwater Pump PID Level Controller

A modular, open-architecture PID-based water level control system for groundwater and sump pump applications.  
This project integrates industrial I/O, variable-frequency drive (VFD) control, and a web-based monitoring interface using a Raspberry Pi 5.

Developed as a Senior Design capstone project at Florida International University.

---

## 📌 Project Overview

Conventional pump control systems rely on float switches or proprietary PLC solutions. Float controls lack visibility and precision, while PLC systems are often cost-prohibitive for small facilities.

This project bridges that gap by implementing:

- Closed-loop PID level control
- Industrial 4–20 mA and 0–10 V signal interfaces
- VFD-based pump speed modulation
- Web-based monitoring and tuning
- Local data logging
- Fail-safe and alarm logic
- Open-source, extensible architecture

A two-barrel hydraulic test rig is used to validate performance under controlled disturbances.

---

## 🔗 Core Libraries & Services

| Dependency | Purpose | GitHub Repository |
|---------|--------|------------------|
| libmodbus | MODBUS RTU/TCP communication with VFDs and industrial devices | https://github.com/stephane/libmodbus |
| Caddy | HTTPS reverse proxy and static web file hosting | https://github.com/caddyserver/caddy |
| Axum (Rust) | High-performance web API backend | https://github.com/tokio-rs/axum |
| PostgreSQL | Structured data storage for logs, configuration, and test results | https://github.com/postgres/postgres |
| Sequent Microsystems Industrial HAT SDK | Hardware access to analog I/O, digital I/O, and RS-485 | https://github.com/SequentMicrosystems/megaind-rpi |

---

## ⚙️ System Architecture

**Core Components**

- Raspberry Pi 5
- Sequent Microsystems Industrial Automation HAT
- Yaskawa GA500 VFD
- Submersible centrifugal pump
- Hydrostatic level transducer (4–20 mA)
- Two-barrel hydraulic test rig
- Local web interface (HTML/JS)
- C/C++ PID control firmware

**Control Loop**

