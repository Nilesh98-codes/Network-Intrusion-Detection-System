# AI-Powered Network Intrusion Detection System

Ever wondered what your network traffic looks like in real time? So did I.

This project is my attempt at building a real-time Network Intrusion Detection System (IDS) using Python. It captures live packets from the network, learns what "normal" traffic looks like using an online machine learning model, and flags anything that seems unusual through an interactive dashboard.

It was definitely one of the more challenging projects I've worked on, but also one of the most rewarding. Along the way I learned a lot about packet sniffing, anomaly detection, and building real-time applications.

---

## ✨ Features

- 📡 Capture live network traffic using **Scapy**
- 🤖 Detect anomalies with **River's Half Space Trees** (online machine learning)
- 📊 Interactive dashboard built with **Gradio**
- 📈 Real-time traffic and intrusion visualizations
- 🚨 Dynamic anomaly scoring instead of a fixed threshold
- 🌐 Protocol distribution analysis
- 🔍 Filter packets by protocol or IP address
- 📋 Live detection log
- 📄 Export incident reports as PDF

---

## 🛠️ Tech Stack

- Python
- Gradio
- Scapy
- River
- Plotly
- FPDF2

---

## 📷 Screenshots

### Dashboard


```
screenshots/dashboard.png
screenshots/dashboard_live.png
screenshots/dashboard_attack.png
```

---

## 🚀 Getting Started

Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/Network-Intrusion-Detection-System.git
```

Move into the project folder

```bash
cd Network-Intrusion-Detection-System
```

Install the required packages

```bash
pip install -r requirements.txt
```

Run the application

```bash
python app.py
```

---

## ⚙️ How It Works

The IDS continuously listens for live network packets using Scapy.

For every packet, a set of network features is extracted and passed into River's **Half Space Trees** anomaly detection model. Instead of relying on predefined attack signatures, the model learns what normal traffic looks like over time and assigns an anomaly score to each packet.

If the score exceeds a dynamic threshold, the packet is flagged as suspicious and the dashboard updates in real time with graphs, statistics, and event logs.

---

## 📁 Project Structure

```
Network-Intrusion-Detection-System/
│
├── app.py
├── IDS.ipynb
├── requirements.txt
├── README.md
├── LICENSE
├── .gitignore
└── screenshots/
```

---

## 🔮 Future Improvements

Some ideas I'd like to explore in the future:

- PCAP file analysis
- Multiple anomaly detection models
- Email or Discord alerts
- Threat classification
- GeoIP visualization
- Database logging
- Docker support

---

## 💭 Final Thoughts

This project definitely pushed me out of my comfort zone.

From debugging packet sniffing issues to experimenting with online machine learning and designing the dashboard, there were plenty of moments where I thought I'd broken everything 😅. In the end, it became one of the most enjoyable projects I've built and taught me a lot about networking, cybersecurity, and real-time data processing.

If you have any suggestions or ideas for improvements, I'd love to hear them!

---

## 📜 License

This project is licensed under the MIT License.