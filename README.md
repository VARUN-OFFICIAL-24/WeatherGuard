# 🌪️ WeatherGuard AI  
### Intelligent Weather Monitoring & Disaster Response System

WeatherGuard AI is an AI-powered decision-support system that monitors real-time weather conditions, analyzes potential disaster risks, and generates coordinated emergency response plans with human oversight.

> ⚠️ This project is designed for **assistance and planning purposes only**. It does not replace official emergency or meteorological systems.

---

## 🎯 Problem Statement

Weather-related disasters often suffer from:
- Delayed response planning
- Fragmented coordination between departments
- Lack of explainable, auditable decisions
- Alert fatigue caused by false positives

WeatherGuard AI addresses these challenges by combining real-time weather data with AI-driven analysis and controlled decision workflows.

---

## ✨ Key Features

- 🌦️ **Real-Time Weather Monitoring**  
  Fetches live weather data using the OpenWeatherMap API.

- 🤖 **AI-Based Disaster Classification**  
  Uses a local Large Language Model (Llama 3.2 via Ollama) to interpret weather conditions and classify disaster types.

- 🚨 **Severity Assessment**  
  Automatically categorizes events into:
  - Critical
  - High
  - Medium
  - Low

- 🏢 **Department-Level Response Planning**  
  Generates response strategies for:
  - Emergency Response
  - Public Works
  - Civil Defense

- 👤 **Human-in-the-Loop Verification**  
  Human approval is required for low and medium severity alerts to prevent false alarms.

- 📧 **Automated Email Alerts**  
  Sends structured alerts with weather details, risk assessment, and recommended actions.

- 📝 **Logging & Audit Trail**  
  All decisions and alerts are logged for transparency and post-event analysis.

---

## 🧠 How It Works (High-Level)

1. Weather data is collected from a live API  
2. AI analyzes the data to identify potential disasters  
3. Severity level is assessed  
4. Events are logged for auditing  
5. Responses are generated and routed  
6. Human approval is requested if required  
7. Alerts are sent upon approval  

---

## 🧩 Technology Stack

- Python 3.8+
- LangChain
- LangGraph
- Ollama (Local LLM)
- OpenWeatherMap API
- SMTP (Email notifications)
- dotenv (Secrets management)

---

## ⚙️ Installation

### Prerequisites
- Python 3.8 or higher
- pip
- OpenWeatherMap API key
- Gmail account (for email alerts)
- Ollama installed locally

---

### Clone the Repository

```bash
git clone https://github.com/yourusername/weatherguard-ai.git
cd weatherguard-ai
```

---

### Install Dependencies

```bash
pip install -r requirements.txt

```

---


### Install Ollama & Model

```bash
curl -fsSL https://ollama.com/install.sh | sh
ollama pull llama3.2

```

---


### 🔐 Configuration
  Create a .env file in the project root.

```bash
OPENWEATHER_API_KEY=your_api_key_here

SENDER_EMAIL=your_email@gmail.com
RECEIVER_EMAIL=receiver@gmail.com
EMAIL_PASSWORD=your_gmail_app_password

OLLAMA_HOST=http://localhost:11434

```
> 🔒 Do not commit the .env file to GitHub.

---

### 🚀 Usage
  Run the system using:

```bash
python disaster_system.py
```
  When prompted, enter one or more cities to monitor:

```bash
Enter cities to monitor: London Tokyo Mumbai

```
---


### 📧 Alert Example

```bash

Weather Alert: High Severity Event – Mumbai

Disaster Type: Severe Storm
Severity Level: High

Key Conditions:
- Wind Speed: 20 m/s
- Humidity: 88%
- Pressure: 1006 hPa

Recommended Actions:
- Activate emergency response teams
- Alert civil defense authorities
- Prepare infrastructure safety measures

```
---

## 📝 Logging

The system maintains logs for:
- Weather data
- Disaster classification
- Severity decisions
- Approval outcomes
- Alert dispatch status

Logs can be used for audits, analysis, and future improvements.
---

## ⚠️ Limitations

- Dependent on third-party weather APIs
- AI outputs may vary across runs
- Not intended for autonomous real-world deployment
- Requires human oversight

---

## Future Enhancements

- Web-based monitoring dashboard
- SMS and push notifications
- GIS-based disaster visualization
- Predictive risk modeling
- Multi-language support
- IoT weather station integration


---

### 📄 License

This project is licensed under the MIT License.

---

### ⚠️ Disclaimer

WeatherGuard AI is an experimental decision-support system intended for research, education, and prototyping. Always rely on official authorities for emergency actions.

---
















