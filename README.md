Vision and aim: Explainable Root Cause Analysis Engine for Enterprise Systems

Roadmap: (This is an AI assisted project and not a research paper or publication)

-- 2026-27: Build automated RCA and redeployment of complex multi-layered enterprise technology (software) systems using RCA from LLMs and redeploy using DevSecOps automation - keep human in the loop 

-- 2027-28: Include mathematics including Markov Chains → State transitions & fault propagation, Time Series Models → Trend, anomaly detection, Bayesian Inference → Probabilistic reasoning & RCA and Graph Models (GNN/Knowledge Graphs) → Dependency mapping - build analytics using this and feed into RCA after profiling the complex system 

-- 2028-29: Extrapolate to Electrical systems (grids, PLCs, SCADA), Electronics systems (embedded devices, IoT) and Technology systems (applications, microservices, cloud infra) - Generalize using above two steps 

-- 2030-31: Create a generic framework and publishable work in journals and conferences for the above 

Trademark Notice:

All third-party product names, logos, and brands are property of their respective owners. Use of these names, logos, and brands does not imply endorsement.
Open Source Logos Attribution

This project may include logos, trademarks, and brand assets of third-party open-source technologies for identification and informational purposes only.

All such logos and trademarks are the property of their respective owners, including but not limited to:
The Apache Software Foundation (e.g., Tomcat)
NGINX, Inc. / F5 (e.g., NGINX)
PostgreSQL Global Development Group (e.g., PostgreSQL)
The OpenTelemetry Project (e.g., OpenTelemetry)
The Linux Foundation / CNCF (where applicable)
Other respective open-source projects and foundations

These logos are used solely to represent the technologies referenced in this project and do not imply any affiliation, endorsement, or sponsorship.

All rights, including trademark rights, remain with the respective owners. Users must comply with individual trademark and brand usage guidelines when reusing such logos.

PROJECT CONTEXT
This project was started as part of the Executive Masters in Data Science for Decision Making at IIT Gandhinagar - DSDM | IITGNX in October, 2025

Status:

Change log: 

v0.9_1 – 18th April 2026 (WIP / Draft)

v0.9_2 – 21st  April 2026 (WIP / Draft) - Prompt 7 added and related section on literature review added in the end 

v0.9_3 – 21st  April 2026 (WIP / Draft) - Prompt 8 added and related section on research question / hypothesis

This is a practical project concept note and implementation plan, not a formal research paper. Will convert into a research paper and PhD thesis later (maybe as time and work progressses). 

Prompts and thinking used for proposal:

1. Generic framework and implementation template for automated debugging and redeployment for electrical, electronics & technology systems assisted by models formed by Markov Chains, Time Series, Bayesian and Graphs Expand and build a 5 page proposal, refine as necessary 

2. Give me some relevant research papers on this 

3. Give me list of important 50 concepts from mathematics, science & engineering for this research 

4. Talk to me about a crawler like Google Spider - Apache Nutch which can map and build graphs for electrical, electronic & technology systems - how will we build it, maintain, enhance it, how we will write contracts, etc. for all major systems to interface with for debugging 

5. Integrate SHODAN into this

6. Yes please do that 

7. Proposal: Generic Framework for Automated Debugging & Redeployment of Electrical,
 Electronics & Technology Systems Using Probabilistic and Graph-Based Models
Conduct literature review for above and give me top 15-25 papers on this with tentative research gaps - 3 to 4

8. Generic Framework for Automated Debugging & Redeployment of Electrical, Electronics & Technology Systems Using Probabilistic and Graph-Based Models
Frame a research question / hypothesis for the above

***********************************

---

```markdown
# 🚀 Automated Debugging & RCA Framework (Agentic AI)

A **minimal agentic AI framework** for automated debugging, root cause analysis (RCA), and evidence-driven diagnostics across:

- Web applications  
- Infrastructure (OS + DB)  
- Browser-level behavior (CDP)  
- SSL/TLS validation  

---

## 🎯 Objective

To demonstrate a **working, explainable debugging system** that:

- Collects **multi-layer evidence**
- Correlates signals across systems
- Uses LLMs for **structured RCA**
- Produces **human-readable execution reports**

---

## 🧠 Architecture Overview

```

```
            +----------------------+
            | Agent Orchestrator   |
            | (agentic_orchestrator.py) |
            +----------+-----------+
                       |
---------------------------------------------------------
|            |               |                |
v            v               v                v
```

CDP Agent   LLM Debug     OS + DB RCA     SSL/TLS Agent
(debug_site  (llm_debug)   (os_db_debug)   (ssl_check)
_cdp.py)

```
                       |
                       v
            +----------------------+
            | Final LLM Report     |
            +----------------------+
```

```

---

## 📂 Project Structure

```

.
├── agentic_orchestrator.py
├── debug_site_cdp.py
├── llm_debug.py
├── os_db_debug.py
├── ssl_check.py
├── debug_env.py
└── agentic_output/

````

---

## ⚙️ Core Components

---

### 1. 🧩 Agent Orchestrator

**File:** `agentic_orchestrator.py`

**Role:**
- Central execution engine
- Runs all agents sequentially
- Aggregates results
- Generates final RCA report using LLM

**Agents executed:**
1. CDP Capture  
2. Website Debug (LLM-assisted)  
3. OS + MySQL RCA  
4. SSL/TLS Validation  
5. Final Report Generator  

**Output:**
- `agentic_execution_report.json`
- `agentic_execution_report.md`

---

### 2. 🌐 CDP Deep Debug Agent

**File:** `debug_site_cdp.py`

**Role:**
- Uses Chrome DevTools Protocol (CDP)
- Captures deep browser-level diagnostics

**Captures:**
- Network requests/responses  
- Console logs  
- JavaScript exceptions  
- Performance metrics  
- Screenshots  
- Response bodies  

**Key capability:**
> Full browser observability without manual DevTools usage

---

### 3. 🤖 LLM-Powered Website Debugging

**File:** `llm_debug.py`

**Role:**
- Collects structured evidence
- Uses LLM to generate RCA

**Probes:**
- DNS resolution  
- HTTP response chain  
- TLS socket inspection  
- Chrome/CDP probe  

**Output:**
- Structured debugging evidence  
- LLM-generated RCA:
  - Root cause  
  - Evidence  
  - Fix steps  
  - Severity  

---

### 4. 🖥️ OS + Database RCA Agent

**File:** `os_db_debug.py`

**Role:**
- Performs system-level RCA on:
  - Windows OS  
  - MySQL database  

**Collects:**
- CPU, memory, disk, network  
- Top processes  
- Windows event logs  
- MySQL status + variables  
- InnoDB lock/deadlock signals  

**RCA Logic:**
- Rule-based heuristics  
- Threshold-driven anomaly detection  

**Example findings:**
- CPU saturation  
- Memory pressure  
- MySQL connection storms  
- Slow query spikes  
- Deadlocks  

---

### 5. 🔐 SSL / TLS Validation Agent

**File:** `ssl_check.py`

**Role:**
- Validates SSL/TLS correctness using real browser behavior

**Checks:**
- Certificate validity  
- Hostname matching (SAN / wildcard)  
- TLS protocol + cipher  
- Certificate errors from browser  

**Key insight:**
> Uses browser-level truth instead of just OpenSSL checks

---

### 6. 🔑 Environment Debug

**File:** `debug_env.py`

**Role:**
- Verifies environment configuration  
- Checks availability of `OPENAI_API_KEY`  

---

## ▶️ How to Run

### 1. Install dependencies

```bash
pip install requests websocket-client psutil mysql-connector-python openai
````

For Windows:

```bash
pip install pywin32 wmi
```

---

### 2. Set OpenAI API Key

```bash
# Windows PowerShell
$env:OPENAI_API_KEY="your_key_here"
```

---

### 3. Run orchestrator

```bash
python agentic_orchestrator.py
```

---

## 📊 Output

Generated in:

```
agentic_output/
```

### Files:

* `agentic_execution_report.json`
* `agentic_execution_report.md`

---

## 🧪 Example Output (Simplified)

```
Root Cause: SSL hostname mismatch

Confidence: High

Evidence:
- Certificate SAN does not match domain
- Browser TLS validation failed

Fix:
- Update certificate SAN entries
- Reissue certificate
```

---

## 🧠 Key Design Principles

* Multi-layer observability
* Evidence-driven RCA
* Explainable AI (not black-box)
* Agent-based modular design
* Human-in-the-loop friendly

---

## ⚠️ Limitations

* Sequential execution (not parallel yet)
* Rule-based RCA (partial)
* No real-time streaming
* No production hardening
* Requires local Chrome installation

---

## 🚀 Future Enhancements

* Parallel agent execution
* Bayesian / probabilistic RCA
* Graph-based dependency modeling
* Kubernetes + distributed tracing support
* UI dashboard
* Auto-remediation (with safeguards)

---

## 🎯 Positioning

**Explainable Root Cause Analysis Engine for Enterprise Systems**

---

## 🧨 Disclaimer

* This tool is for debugging and analysis only
* Does NOT perform automatic remediation
* Should be used in controlled environments

---

## 👤 Author

Neil Harwani
Enterprise AI Architect & Systems Thinker

---

## ⭐ Final Note

This project demonstrates a working foundation for agentic debugging systems combining:

* Observability
* Systems thinking
* AI reasoning

```
