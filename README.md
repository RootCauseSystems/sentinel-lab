# Project Sentinel-1: AI Security Research Lab

**Status:** Active | **Focus:** LLM Red Teaming & Adversarial Defense

## 🛡️ Mission
To analyze vulnerabilities in local Large Language Models (LLMs) and develop middleware defenses against Prompt Injection, Jailbreaks, and Social Engineering attacks.

## 🏗️ Architecture
* **Engine:** Ollama (running Llama 3.2)
* **Infrastructure:** Local Linux Server with AMD GPU Acceleration.
* **Defense Layer:** Custom Python Middleware (FastAPI/Scripts) for Input Sanitization.
* **Red Team Tools:** Garak (LLM Vulnerability Scanner), Manual Payload Testing.

## 📂 Key Components
* `defense.py`: An interception layer that sanitizes user inputs before they reach the model.
* `attacks/`: Documentation of successful jailbreak prompts (Red Team findings).
* `logs/`: Sanitized logs of blocked adversarial attempts.

## 🚀 Usage (Security Middleware)
This project uses `uv` for modern Python dependency management.

```bash
# Clone the repo
git clone [https://github.com/RootCauseSystems/sentinel-1.git](https://github.com/RootCauseSystems/sentinel-1.git)
cd sentinel-1

# Install dependencies
uv sync

# Run the Defense Console
uv run defense.py