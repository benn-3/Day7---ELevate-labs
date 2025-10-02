# DevOps Task 7 – System Monitoring with Netdata

This project sets up **Netdata** inside Docker to monitor system performance, resource usage, and Docker containers in real time.

---

## 🚀 Setup Instructions

1. Pull the Netdata Docker image:
   ```bash
   docker pull netdata/netdata


RUN the NETDATA Cointainer 

docker run -d --name=netdata \
  -p 19999:19999 \
  --cap-add SYS_PTRACE \
  --security-opt apparmor=unconfined \
  -v netdataconfig:/etc/netdata \
  -v netdatalib:/var/lib/netdata \
  -v netdatacache:/var/cache/netdata \
  -v /etc/passwd:/host/etc/passwd:ro \
  -v /etc/group:/host/etc/group:ro \
  -v /proc:/host/proc:ro \
  -v /sys:/host/sys:ro \
  -v /etc/os-release:/host/etc/os-release:ro \
  netdata/netdata

Access the dashboard:
Open your browser and go to:

http://localhost:19999


📊 Monitoring Screenshots
1. CPU and Memory Usage

2. Disk & Network Metrics

3. Docker Container Metrics
