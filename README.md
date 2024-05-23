# Docker Logs Monitoring Repository

This repository is designed for monitoring Docker container logs directly in Grafana using Docker Compose, Loki, and Promtail as services.

## Setup and Usage

Follow the steps below to set up and use the monitoring system:

### 1. Make sure you have docker and docker-compose installed in the system , if not 
```bash
sudo apt-get update && \
sudo apt-get install -y ca-certificates curl gnupg lsb-release && \
sudo mkdir -p /etc/apt/keyrings && \
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg && \
echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null && \
sudo apt-get update && \
sudo apt-get install -y docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin && \
sudo docker run hello-world && \
docker compose version
```

### 2. Clone the Repository

Clone the repository and start the services by running the following command:

```bash
git clone <repository_url>
```
```bash
cd <repository_directory>
```
* Make sure you check your port numbers in docker-compose.yml file
```bash
docker-compose up -d
```
or 
```bash
docker compose up -d
```

### 3. Access Grafana
Open your web browser and navigate to:
```bash
http://localhost:3000
```
### 4. Grafana Credentials
Use the default credentials to log in:
```bash
Username: admin
Password: admin
```

### 5. Add Dashboard:
* Navigate to the dashboards section in Grafana.
(Select the option to add or upload a dashboard.)
* Use the dashboard template provided in the repository (docker-logs-dashboard.json). This template is pre-configured with queries to display logs from various running containers running .

### 6. Ready to Monitor:
* Your setup is now complete. You should be able to monitor the Docker container logs directly from the Grafana dashboard.
