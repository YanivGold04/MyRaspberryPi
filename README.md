# Raspberry Pi Monitoring with Prometheus & Grafana

This is a personal project I built to monitor my Raspberry Pi using Prometheus and Grafana, all running in Docker containers.  
It helps me keep track of my Pi’s health (CPU, memory, disk, temperature) in real time through a beautiful dashboard.

## Project Goals
- Learn how to monitor Linux systems using Prometheus and Grafana
- Automate everything with Docker Compose
- Practice basic IT and infrastructure concepts hands-on

## Tech Stack
- Raspberry Pi (running Linux)
- Docker + Docker Compose
- Prometheus – collects metrics
- Node Exporter – exposes system metrics
- Grafana – displays dashboards and graphs

## How to Run

### 1. Clone the repository
```bash
git clone https://github.com/yourusername/pi-monitoring.git
cd pi-monitoring
```

### 2. Start the stack
Make sure Docker and Docker Compose are installed on your Raspberry Pi, then run:
```bash
docker compose up -d
```

This will start three containers:
- `prometheus` – the metrics collection service
- `node-exporter` – the system metrics exporter
- `grafana` – the dashboard visualization tool

### 3. Access Grafana
Open your browser and go to:
```
http://<your Pi's IP>:3000
```

Default credentials:
- **Username**: `admin`
- **Password**: `admin` (you'll be prompted to change it)

### 4. Add Prometheus as a Data Source
In Grafana:
- Go to ⚙ **Configuration** → **Data Sources**
- Click **Add data source**
- Choose **Prometheus**
- Set the URL to:  
  ```
  http://prometheus:9090
  ```
- Click **Save & Test** – you should see a success message.

### 5. Import a Dashboard
You can import a ready-made dashboard to visualize the data:
- Go to **Dashboards** → **Import**
- Paste this ID: `1860`
- Click **Load** and select Prometheus as the data source

## What I Learned
This project helped me get hands-on with:
- Docker Compose for service orchestration
- Monitoring tools like Prometheus and Grafana
- Understanding system metrics (CPU, RAM, disk usage, temperature)
- IT infrastructure and automation concepts

## Screenshots
![image](https://github.com/user-attachments/assets/8ebbdc1f-a84b-4b34-a717-684fc53be0a9)


## Credits
- [Prometheus](https://prometheus.io/)
- [Grafana Labs](https://grafana.com/)
- [Raspberry Pi Foundation](https://www.raspberrypi.com/)
