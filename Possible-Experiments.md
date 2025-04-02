#  RF, Drone, and SDR Experiments with Splunk Integration

This document outlines a variety of home lab experiments using the following gear:

-  Windows laptops running Splunk Universal Forwarder
-  RTL-SDR (Software Defined Radio)
-  FPV drones (Walksnail, analog VTX, Crossfire RX)
-  Multiple HF radios (e.g., for FT8, WSPR, JS8Call)

Each section provides ideas for experimentation, data collection, and optional Splunk integrations.

---

###  Radio & SDR Projects

### 1. Spectrum Surveillance / RF Waterfall Logging
- Use RTL-SDR to scan ISM bands, amateur radio, FM, ADS-B, etc.
- Log frequency power levels over time.
- Visualize spectrum activity trends in Splunk dashboards.

### 2. HF Propagation Monitoring
- Log FT8/WSPR/JS8Call contact data.
- Correlate contacts with time of day and band conditions.
- Create Splunk dashboards for propagation analysis.

### 3. RF Fingerprinting / Signal Detection
- Detect known signals like Crossfire RX or Walksnail VTX.
- Alert on signal anomalies or new RF activity using Splunk.

### 4. ADS-B Aircraft Tracking
- Use `dump1090` with RTL-SDR to track aircraft.
- Log aircraft data into Splunk for map visualizations.

---

##  FPV Drone Telemetry & Signal Experiments

### 1. VTX Channel Occupancy Logging
- Use RTL-SDR to scan 5.8 GHz VTX channels.
- Track channel usage frequency over time.
- Prevent overlap and improve multi-pilot coordination.

### 2. Crossfire RX Telemetry Logging
- Log GPS, RSSI, and LQ from Crossfire RX.
- Ingest into Splunk for telemetry visualization.

### 3. Drone Tracking + Signal Mapping
- Combine GPS with Crossfire/Walksnail data.
- Visualize flight paths and RF link quality in Splunk dashboards.

### 4. RF Interference Analysis
- Scan the RF environment during flights using RTL-SDR.
- Correlate interference spikes with telemetry or link dropouts.

---

##  Splunk + SDR/Drones = RF SIEM

### 1. RF SIEM Dashboard
- Ingest data from RTL-SDR, drones, and laptops into Splunk.
- Detect rogue transmitters, signal jamming, and spectrum changes.

### 2. RF Forensics and Replays
- Record IQ data with RTL-SDR during interesting events.
- Re-analyze later with GNU Radio or SDR#.

### 3. Threat Hunting in the Airwaves
- Detect unauthorized Walksnail or analog signals in your area.
- Alert on unknown or misconfigured transmitters.

---

##  Windows Laptop (Splunk Forwarder) Experiments

### 1. Centralized System Monitoring
- Collect logs from laptops: system, network, USB, application logs.
- Correlate activity with drone use or SDR scans.

### 2. RF-Aware Asset Tracking
- Log seen SSIDs, Bluetooth devices, and network changes.
- Track environmental RF shifts over time.

---

##  Crossover Projects

### 1. Jamming Detection & Response Simulation
- Simulate low-power jamming (legal, controlled).
- Detect jamming with SDR + telemetry drop from drones.
- Create Splunk alerts for active interference events.

### 2. RF Range Testing Framework
- Fly drones at set distances and log telemetry and SDR scans.
- Analyze signal strength vs. distance in Splunk.

### 3. Wi-Fi and VTX Band Coexistence Analysis
- Scan 2.4 GHz and 5.8 GHz bands with SDR.
- Use laptops to log Wi-Fi congestion.
- Compare with VTX quality during flights.

---

##  Recommended Tools

- **GNU Radio** – SDR experimentation and signal processing
- **DragonOS** – SDR-focused Linux distro
- **JS8Call / FT8 / WSPR** – Digital HF communication experiments
- **Betaflight / Agent Lite** – Drone telemetry integration
- **Python + Splunk HEC** – Custom data ingestion
- **TinySA / RF Explorer** – Additional RF spectrum tools

---

##  Folder Organization Suggestion (for this Repo)
