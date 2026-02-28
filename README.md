# Automated Bug Report Generator from Error Logs (n8n Workflow)

This repository contains a complete n8n workflow that automates the generation of structured bug reports from raw error logs using AI.

## 🔗 Repository Description
**Project Link:** [https://github.com/NiteshBawane/Automated-Bug-Report-Generator-from-Error-Logs]

## 🎯 Problem Statement
Manual bug reporting is a bottleneck. This workflow reads error logs, analyzes them via an LLM (QA Engineer role), and outputs a formatted report (Title, Severity, Steps to Reproduce, Expected vs Actual Result).

## 📊 Evaluation Criteria Met
- **Approach**: Correct node selection (Trigger -> AI Agent -> Groq LLM).
- **Logical Flow**: Seamless data transition from raw input to structured output.
- **Output Quality**: Strict constraints to prevent hallucinations and maintain fixed formatting.

## 🚀 Workflow Details
- **Trigger**: Chat Trigger (Manual/Chat Input).
- **AI Model**: Groq `llama-3.3-70b-versatile` (High context, fast inference).
- **Prompt Engineering**: QA Engineer persona with strict formatting rules.
- **Anti-Hallucination**: "Use ONLY the log data provided. Mark unknown fields as [UNKNOWN]".

## 🛠️ Installation
1.  **Download JSON**: Grab `automated_bug_report_generator.json`.
2.  **Import to n8n**: Use the 'Import from File' option in your n8n dashboard.
3.  **Configure Credentials**:
    - Select the Groq Chat Model Node.
    - Create new credentials for 'Groq API'.
    - Use your provided API key: `gsk_mFR8...` (keep this secure).
4.  **Test**: Input any error log or use the example provided in the problem statement.
