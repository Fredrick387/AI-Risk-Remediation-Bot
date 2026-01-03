# 🤖🛡️ AI Risk & Remediation Bot  
**Automated CIS / STIG Compliance Analysis & Prioritization**

---

## 📌 Executive Summary

The **AI Risk & Remediation Bot** ingests CIS or STIG compliance scan data and automatically enriches each control with a clear audit title, risk assessment, remediation guidance, and prioritized scoring.  
The tool transforms raw compliance output into **executive-ready, analyst-friendly Excel reports** that support remediation planning, risk discussions, and audit preparation.  
This project demonstrates a practical application of AI in **GRC, security operations, and vulnerability management workflows**.

---

## 🎯 Project Objectives

- Automate interpretation of CIS / STIG audit findings  
- Generate clear, human-readable audit titles  
- Produce concise brief descriptions and remediation guidance  
- Assign **Risk, Difficulty, and Priority** scores automatically  
- Output **clean, presentation-ready Excel reports** with formatting applied  

---

## 🧭 Scope & Environment

- **Input:** CIS / STIG CSV scan exports  
- **Output:** Formatted Excel (.xlsx) analysis reports  
- **Operating System:** Windows  
- **Language:** Python  
- **AI Provider:** OpenAI API  

---

## 🧠 Project Overview

This tool was built to solve a common compliance pain point:  
raw scan data is dense, repetitive, and difficult to translate into actionable remediation work.

The AI Risk & Remediation Bot analyzes each control, interprets its intent, and outputs:
- A short, meaningful **Audit Title**
- A **Brief Description** explaining what is enforced and why it matters
- A **Proposed Solution** written in plain language
- A **Risk Rating**, **Difficulty Level**, and **Priority Score**

The result is a report that can be handed directly to engineering, security leadership, or auditors.

---

## 🔄 Data Flow & Architecture

1. User selects a CIS / STIG CSV file  
2. Python parses compliance-related findings  
3. Each control is sent to AI for semantic analysis  
4. AI returns structured JSON output  
5. Priority score is calculated locally  
6. A new Excel file is generated with:
   - Wrapped text
   - Column sizing
   - Readable layout
   - Timestamped filename  

---

## ⚖️ Scoring & Prioritization Logic

### 🛑 Risk Weighting

| Risk Level | Weight |
|-----------|--------|
| Critical  | 4      |
| High      | 3      |
| Medium    | 2      |
| Low       | 1      |

### 🧩 Difficulty Weighting

| Difficulty | Weight |
|-----------|--------|
| Easy      | 1      |
| Medium    | 2      |
| Hard      | 3      |

### 📊 Priority Formula

Priority = (Risk Weight × 10) − Difficulty Weight


This ensures that:
- High-impact, easy fixes surface first  
- Harder remediations are deprioritized unless risk is severe  

---

## 📑 Output Report Structure

Each row in the Excel report includes:

- Audit ID  
- Audit Title  
- Brief Description  
- Proposed Solution  
- Risk  
- Difficulty  
- Priority Score  
- Quick Win (Yes / No)  
- Rationale  

Formatting is applied automatically:
- Text wrapping for long fields  
- Column widths optimized for readability  
- No manual cleanup required  

---

## 🖼️ Screenshots

> _(Placeholders — replace with your own screenshots)_

### 📊 Example Excel Output – Overview
![Excel Overview Screenshot](screenshots/excel-overview.png)

### 🧠 AI-Enriched Control Detail
![Excel Detail Screenshot](screenshots/excel-detail.png)

---

## 🧪 Use Cases

- Compliance remediation planning  
- Audit preparation and evidence review  
- Security posture reporting  
- GRC automation demonstrations  
- Portfolio project for cybersecurity roles  

---

## 🚀 Future Enhancements

- MITRE ATT&CK technique mapping  
- Remediation owner assignment  
- SLA-based prioritization  
- Dashboard visualizations  
- Support for additional scanner formats  

---

## 📎 Analyst Notes

- Designed as a **Minimum Viable Product (MVP)** with real-world applicability  
- Emphasizes clarity, prioritization, and analyst efficiency  
- Suitable for interviews, demos, and portfolio review  

---

