# Netdata Docker Monitoring

## Overview

This project demonstrates how to install and use Netdata (open-source, real-time monitoring) to visualize and analyze system and application metrics—including CPU, memory, disk, and Docker container stats—using Docker for rapid deployment.

## Objective

- Set up lightweight, real-time system and Docker container monitoring using Netdata.
- Visualize resource usage and performance metrics directly from a browser dashboard.
- Learn to use Netdata’s dashboard, chart panels, and alerting capabilities for DevOps/automation workflows.

## Prerequisites

- Docker installed on your system (Windows, Linux, or Mac).

## Installation Steps

1. Pull and run the official Netdata Docker image (this exposes the Netdata UI on port 19999):
    ```sh
    docker run -d --name=netdata -p 19999:19999 netdata/netdata
    ```
2. Verify the Netdata container is running:
    ```sh
    docker ps
    ```

## Access the Dashboard

- Open a browser and go to:  
  ```
  http://localhost:19999
  ```
- You’ll see real-time charts for:
    - CPU, memory, disk usage
    - Docker container stats (running, stopped, health status)
    - Network activity and system processes.

## Monitoring Features

- **System Metrics:** CPU load, RAM utilization, disk I/O, file system stats, network bandwidth.
- **Docker Metrics:** Total containers, states (running/paused/exited), health, image usage, per-container CPU/memory/network.[5]
- **Alarms/Alerts:** Netdata comes with built-in alarms for high usage, system failures, etc. Explore via the Alerts/Health tabs on the dashboard.
- **Logs:**  
  Container logs and Netdata event logs can be inspected using:
    ```sh
    docker exec -it netdata bash
    less /var/log/netdata/error.log
    ```

## Screenshot
### screenshot-1: In terminal
<img width="1447" height="558" alt="Screenshot 2025-10-03 120240" src="https://github.com/user-attachments/assets/348334de-5815-40b3-ae27-d8980a41b45c" />

### screenshot-2: Netdata Dashboard
<img width="1905" height="942" alt="Screenshot 2025-10-03 120218" src="https://github.com/user-attachments/assets/11547b6c-c862-4230-8584-e5b8cb0883d6" />




