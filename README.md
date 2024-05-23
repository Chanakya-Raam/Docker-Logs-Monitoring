# Docker Logs Monitoring Repository

This repository is designed for monitoring Docker container logs directly in Grafana using Docker Compose, Loki, and Promtail as services.

## Setup and Usage

Follow the steps below to set up and use the monitoring system:

### 1. Clone the Repository

Clone the repository and start the services by running the following command:

```bash
git clone <repository_url>
```
```bash
cd <repository_directory>
```
```bash
docker-compose up -d
```

2. Access Grafana
Open your web browser and navigate to:
```bash
http://localhost:3000
```
3. Grafana Credentials
Use the default credentials to log in:
```bash
Username: admin
Password: admin
```

4. Add Dashboard:
* Navigate to the dashboards section in Grafana.
(Select the option to add or upload a dashboard.)
* Use the dashboard template provided in the repository (docker-logs-dashboard.json). This template is pre-configured with queries to display logs from various running containers.

5. Ready to Monitor
*Your setup is now complete. You should be able to monitor the Docker container logs directly from the Grafana dashboard.
