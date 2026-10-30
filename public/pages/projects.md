# 🧪 Projects

## [AI-Powered SOC Alert Enrichment Pipeline](https://medium.com/@muzzzz2k3) 🔗
`Home lab · 2026 – Present`

**Flow:** Sysmon → Splunk (UF) → n8n → VirusTotal + Ollama (phi3:mini) → back to Splunk via HEC

- Built a VMware SOC home lab (Windows endpoints, Ubuntu Splunk server) on a dedicated lab subnet.
- Deployed Sysmon with an ATT&CK-tagged configuration (sysmon-modular) for process, network, file, registry, and DNS telemetry.
- Expanded Windows logging: Security 4688 process creation with full command lines, and PowerShell 4104 script block logging to surface decoded `-enc` payloads.
- Forwarded telemetry via Splunk Universal Forwarder into separate `sysmon` and `wineventlog` indexes to keep detection searches scoped and fast.
- Automated alert triage in n8n: Splunk alerts enriched with VirusTotal threat intelligence and summarised by a local LLM (Ollama), with verdicts written back to Splunk through the HTTP Event Collector.
- Documented the build in a [Medium write-up](https://medium.com/@muzzzz2k3).
- **Stack:** Splunk Enterprise, Splunk UF, Sysmon, Windows Event Logging, n8n, VirusTotal API, Ollama, Ubuntu Server, VMware

## [ICT704 CTF War Game — Red vs Blue Team Exercise]() 🔗
- Led the red team in a live Capture the Flag war game against an active blue team.
- Executed a full MITRE ATT&CK kill chain — initial access, privilege escalation, credential dumping, lateral movement, and persistence.
- Used MITRE Caldera as C2 to automate and orchestrate the attack chain across multiple victim VMs.
- Maintained persistent control of the Windows VM via a watchdog cron job despite active blue team defence.
- **Stack:** MITRE Caldera, Parrot OS, Kali Linux, VMware, John the Ripper, Responder, nmap, sshpass

## ICT801 Research — Evaluating LLMs for Security Log Classification
`Master's research · 2026`
- Comparative evaluation of large language models classifying security-relevant vs benign events in public labelled log datasets.
- Controlled experiment under a uniform prompting and evaluation protocol, scored with precision, recall, and F1, plus error analysis of false positives and negatives.
- **Stack:** Python, Pandas, scikit-learn

---

## Other — Web Development

### [Azilfa - Online Jersey Store](https://azilfajerseys.com/) 🔗
- Full-stack MERN e-commerce application with Stripe payment integration.
- **Stack:** MongoDB, Express.js, React.js, Node.js, Stripe API

### [JARVIS - AI Chatbot Assistant](https://jarvis-blond.vercel.app/) 🔗
- AI assistant answering professional queries from personal data via the OpenAI API.
- **Stack:** React.js, OpenAI API

### [ChatEngine - Chatbot Customization Platform](https://chatengine-frontend.vercel.app/) 🔗
- Platform for creating and deploying custom LLM-powered chatbots.
- **Stack:** React.js, LLM APIs, JavaScript
