# 🛡️ URL Phishing Detector

A lightweight desktop application that analyzes URLs in real-time and classifies them as **Safe**, **Suspicious**, or **Dangerous** using a heuristic scoring engine. It features ultra-fast structural analysis with absolutely no network requests and no heavy machine learning models.

---

## Quick Start

### Installation

Install the single required dependency:

```bash
pip install tldextract

python3.11 app.py
bash run.sh

├── app.py           # Tkinter GUI application (Dark theme, score ring, breakdown panel, history)
├── detector.py      # Core heuristic scoring engine (Defines weights, thresholds, and result dicts)
├── features.py      # Feature extraction engine (Extracts ~20 structural signals from raw URL strings)
├── check_syntax.py  # Utility script conducting quick AST syntax checks for app.py
└── run.sh           # Executable launch script tailored for Python 3.11 environment execution


 Important Note: This tool acts as a rapid first line of defense based purely on structural linguistics. It has the following design boundaries:
Static Inspection: It strictly analyzes the textual structure of the URL; it does not connect to the internet, perform page requests, or download code.
Static Reference Data: Keyword and TLD lists are baked into the local code and do not sync with real-time threat intelligence feeds.


some test website link

https://construct01-2c101e675a2f.herokuapp.com/?email=enquiries@devolkitchens.co.uk	Suspicious
http://estradingcorporation.com/	Suspicious
https://www.facebook.com/reel/163697933055110?mibextid=TQi3BacyrYqMRoHa	Suspicious
https://www.facebook.com/reel/163697933055110?mibextid=TQi3BacyrYqMRoHa	Suspicious
https://c1.curix.ai/autograph/new_autograph/26GL1/6OOZBYQ_.html	Suspicious
http://estradingcorporation.com/	Suspicious
https://www.dropbox.com/s/9oop1i4igecambj/upwork-task-123.mp4?dl=0	Clean
https://www.hydrogeninsight.com/policy/eu-delegated-acts-on-green-hydrogen-to-imminently-become-law-after-clearing-european-council-and-parliament-scrutiny/2-1-1467798	Clean
https://go.microsoft.com/fwlink/?LinkId=2086738	Clean
https://dcument.z19.web.core.windows.net/	
