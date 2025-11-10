# AI Powered Firewall Anomaly Detection

A cybersecurity-focused tool that analyzes **firewall logs** to identify suspicious and potentially malicious network activity. This project combines **rule-based anomaly detection** with **LLM-driven threat reasoning** to produce actionable incident reports.

---

## 🔥 Why This Project Matters

Traditional firewalls generate massive amounts of log data — but **security teams rarely have time to manually review them**. Attackers exploit this gap.

This tool detects:

* Repeated connection attempts (brute force / reconnaissance)
* Unusual protocol usage or port scanning
* Traffic from suspicious / external / unknown IP sources
* Sudden lateral movement behavior

Then, the **AI Threat Analyst** explains:

* What the event suggests
* Likely attacker intent
* Impact if ignored
* Recommended defensive response

This makes it suitable for **SOC analysts, Incident Responders, and Security Engineers**.

---

## 🧠 System Architecture

```mermaid
flowchart LR
    A[Firewall Logs (Cisco ASA / Others)] --> B[Log Parser]
    B --> C[Anomaly Detection Engine]
    C --> D[AI Threat Reasoning]
    D --> E[Incident Report Output]
```

---

## 🚀 Features

* Parses real firewall logs
* Detects abnormal network patterns
* Generates **clear human-readable threat reports**
* Supports customization for enterprise rule tuning

---

## 🛠️ Tech Stack

| Component       | Technology                              |
| --------------- | --------------------------------------- |
| Log Parsing     | Python Regex / Structured Extraction    |
| Detection Logic | Statistical & Rule-Based Heuristics     |
| AI Reasoning    | LLM w/ Prompt-Driven Threat Explanation |
| Output          | Markdown Security Incident Report       |

---

## ▶️ How to Run

```bash
python run.py <path_to_firewall_log>
```

Example:

```bash
python run.py sample_logs.log
```

Output report will be saved as:

```
report.md
```

---

## 📄 Example Output Highlights

```
Suspicious Source IP: 203.0.113.24
Pattern: Multiple inbound SSH attempts
Threat Interpretation: Possible brute-force probe
Recommended Action: Geo-block and enable fail2ban or MFA
```

---

## 📌 File Structure

```
/AI-Anomaly-Detection
│ run.py
│ parser.py
│ anomaly_detector.py
│ rag_assistant.py
│ README.md
│ sample_logs.log (optional)
```

---

## 🎯 Future Enhancements

* Add probabilistic anomaly scoring models
* Integrate with SIEM/Elastic dashboards
* Add automated IP reputation lookup

---

## 👤 Author

**Kalpana** — Security & AI Engineering

---

Feel free to fork, improve, or open issues. Contributions are welcome.
