# 🚀 Prometheus Monitoring & Alerting Project

## 📌 Project Overview
This project demonstrates a complete real-time monitoring and alerting setup using Prometheus, Alertmanager, Blackbox Exporter, and a Spring Boot application in a Linux environment.
The objective of this project is to monitor infrastructure, application health, uptime, and service availability while generating automated email alerts whenever issues occur.
This project reflects a production-style monitoring workflow commonly used in DevOps and Cloud environments.

# 🏗️ Architecture
Spring Boot App / Linux Server / External Website
                    ↓
            Prometheus Server
                    ↓
            Alert Rule Engine
                    ↓
              Alertmanager
                    ↓
            Gmail Notifications

# ⚙️ Technologies Used
| Tool | Purpose |
|------|----------|
| Prometheus | Metrics collection & monitoring |
| Alertmanager | Alert routing & notifications |
| Blackbox Exporter | Endpoint & uptime monitoring |
| Spring Boot | Sample monitored application |
| Node Exporter | Linux system metrics |
| Linux (RHEL/Ubuntu) | Monitoring environment |
| Gmail SMTP | Email alert integration |

# 🎯 Features
✅ Real-time monitoring  
✅ Linux server monitoring  
✅ Spring Boot application monitoring  
✅ HTTP/HTTPS endpoint monitoring  
✅ Automated Gmail alerts  
✅ Alert rule configuration  
✅ Blackbox uptime checks  
✅ Infrastructure observability  
✅ Production-style monitoring workflow

# 📂 Project Structure
```bash
prometheus-monitoring-alerting-project/
│
├── prometheus/
│   ├── prometheus.yml
│   └── alert.rules.yml
│
├── alertmanager/
│   └── alertmanager.yml
│
├── blackbox/
│   └── blackbox.yml
│
├── spring-boot-app/
│   └── application.properties
│
├── screenshots/
│   ├── prometheus-dashboard.png
│   ├── alertmanager-ui.png
│   ├── gmail-alert.png
│   └── architecture-diagram.png
│
└── README.md
```

# 🔍 Monitoring Components
## 1️⃣ Prometheus
Prometheus collects metrics from:
- Spring Boot application
- Linux server
- Blackbox Exporter endpoints

It stores metrics as time-series data and evaluates alert rules.
---

## 2️⃣ Alertmanager
Alertmanager receives alerts from Prometheus and sends email notifications using Gmail SMTP.

Example alerts:
- Service Down
- High CPU Usage
- Endpoint Unreachable
- Application Health Failure
---

## 3️⃣ Blackbox Exporter
Blackbox Exporter is used for uptime and endpoint monitoring.

It monitors:
- HTTP/HTTPS endpoints
- Website availability
- DNS response
- SSL certificate status
- TCP connectivity
---

## 4️⃣ Spring Boot Monitoring
Spring Boot Actuator endpoints expose application metrics for Prometheus scraping.

Example endpoint:
```bash
/actuator/prometheus
```
---

# 📧 Email Alert Integration
Gmail SMTP was configured inside Alertmanager to send automated alerts.
Example:
- Target DOWN
- Website unavailable
- Server issues

Alerts are instantly delivered to email.
---

# 🚨 Sample Alert Rules
```yaml
groups:
  - name: system-alerts
    rules:

      - alert: InstanceDown
        expr: up == 0
        for: 1m
        labels:
          severity: critical
        annotations:
          summary: "Target is Down"
```
---

# 🧪 Validation & Testing
The following tests were performed:

- Service shutdown testing
- Endpoint failure simulation
- Prometheus target validation
- Alert delivery testing
- Blackbox uptime verification
---

# 📈 Learning Outcomes
This project helped improve knowledge in:

- Monitoring & Observability
- DevOps Monitoring Tools
- Linux Administration
- Alerting Systems
- Infrastructure Health Monitoring
- Troubleshooting & Incident Detection
---

# 💼 Resume Value
This project demonstrates practical experience with:
- Infrastructure Monitoring
- Production Alerting
- DevOps Operations
- Linux Monitoring
- Application Observability
---

# 👨‍💻 Author
Harsh Sojitra
RHCSA Certified | DevOps & Cloud Enthusiast

