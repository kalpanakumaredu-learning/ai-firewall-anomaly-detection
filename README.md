# AI Powered Firewall Anomaly Detection

## 🛡️ Overview

This project analyzes **firewall logs** to detect and explain **suspicious or malicious network activity**. It is designed to demonstrate practical skills in:

* **Cybersecurity Threat Detection**
* **Network Security Analysis**
* **AI / LLM-based Incident Reasoning**

The system combines **rule-based anomaly detection** with **AI-driven threat interpretation**, producing clear security incident reports suitable for SOC workflows.

---

## 🚀 Key Capabilities

* Parses raw firewall logs and extracts relevant network events
* Detects anomalies (e.g., repeated failed access, port scans, lateral movement attempts)
* Uses AI to explain *intent*, *risk*, and *recommended defense actions*
* Generates a clean **`report.md`** for documentation or incident response handoff

---

## 🧠 Architecture

```
          +--------------------------+
          |      Firewall Logs       |
          +------------+-------------+
                       |
                       v
              +--------+--------+
              |   Log Parser    |
              +--------+--------+
                       |
                       v
              +--------+--------+
              | Anomaly Detector|
              +--------+--------+
                       |
                       v
              +--------+--------+
              |  AI Threat Intel|
              | (LLM / RAG)     |
              +--------+--------+
                       |
                       v
               Generates report.md
```

---

## 📦 Tech Stack

| Component            | Technology                       |
| -------------------- | -------------------------------- |
| Programming Language | Python 3                         |
| Log Parsing          | Custom Rule & Regex Parsing      |
| Anomaly Detection    | Statistical / Rule-based Scoring |
| AI Threat Reasoning  | LLM / RAG Workflow               |

---

## 🏃‍♀️ How to Run

```bash
python run.py <path_to_firewall_log>
```

Example:

```bash
python run.py sample_logs.log
```

Output will be written to:

```
report.md
```

---

## 📝 Example Detection Output

* Source IP flagged due to repeated failed SSH connection attempts
* AI analysis explains:

  * Possible attacker intent
  * Threat level
  * Potential system impact
  * Recommended mitigation steps

---

## 📁 Project Structure

```
├── parser.py           # Extracts structured fields from raw firewall log lines
├── anomaly_detector.py # Identifies suspicious patterns
├── rag_assistant.py    # Generates human-readable threat explanation
├── run.py              # Main executable
└── README.md           # Project documentation
```

---

## 🔥 Future Improvements

* Real-time streaming analysis (SIEM integration)
* Dashboard visualizations
* Model fine-tuning with organization-specific network baselines

---

## 👤 Author

**Kalpana**
Cybersecurity & AI Security Engineering

---

Feel free to contribute, enhance, or discuss improvements via Issues and Pull Requests.
