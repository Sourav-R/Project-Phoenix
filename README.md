# Project-Phoenix: AI-Driven Knowledge Synthesis & Skill Recovery
 
🔍 Overview
Project Phoenix is a self-hosted AI automation pipeline designed to solve a critical challenge in cybersecurity: Technical Knowledge Decay. Following a significant data loss of professional artifacts, I engineered this system to audit, transcribe, and index four semesters of academic archives (Master of Cybersecurity) and live demonstration videos.

The system uses a Locally Hosted Large Language Model (LLM) to perform a forensic audit of my own "Nightmare" notes—specifically from Network Security, IT Forensics, and Cloud Security—to reconstruct a searchable Private SOC Vault and a polished Public Portfolio.

🛠️ The Stack
Infrastructure: Parrot OS (Debian-based Security Distro)

Containerization: Docker & Docker Compose (Optimized for Intel i7 11th Gen)

Orchestration: n8n (Self-hosted)

Intelligence: Ollama running Mistral-Nemo (12.2B)

Transcription: OpenAI Whisper (Local) for "Live Demo" video-to-text conversion

Data Source: Microsoft OneDrive API Integration

⚙️ How it Works (The Pipeline)
Discovery: n8n scans legacy OneDrive archives for technical project reports, lab notes, and demonstration videos.

Extraction:

Text: PDFs and Markdown files are parsed for raw CLI commands (nmap, tcpdump, iptables).

Video: Live demo audio is transcribed locally via Whisper to capture "spoken troubleshooting logic."

Reasoning (The AI Audit): Mistral-Nemo categorizes the data into "Portfolio Buckets":

Bucket A: Network Defense & Packet Analysis

Bucket B: Digital Forensics & Incident Response (DFIR)

Bucket C: VAPT & Offensive Security

Synthesis:

The Vault: Generates a private technical Wiki for real-time reference during SOC shifts at ThIRU.

The Portfolio: Automatically drafts professional project cards mapped to NIST and MITRE ATT&CK frameworks.

🏗️ Technical Troubleshooting (The "Log")
During the build, several production-level hurdles were overcome:

Daemon Conflict: Identified and resolved a podman.sock redirection conflict to restore Docker API connectivity.

Repository Optimization: Successfully mapped official Docker repositories to the Parrot OS "Echo" (Debian 13) environment using compatible "Bookworm" (Debian 12) release files.

Resource Management: Engineered "Split in Batches" logic in n8n to manage CPU thermals during 8+ hour LLM inference runs.

📊 Results (The Recovery)
Reclaimed Skills: [X] specific networking tools rediscovered and indexed.

Evidence: [Y] live demonstration videos converted into technical blog posts.

Operational Readiness: Reduced "Time-to-Recall" for legacy technical protocols by ~90%.

"In cybersecurity, your value isn't just what you know—it's how fast you can find what you've forgotten."
