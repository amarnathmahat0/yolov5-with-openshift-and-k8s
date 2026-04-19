# 🚀 YOLOv5 Deployment on OpenShift & Kubernetes

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)](https://www.python.org/)
[![Docker](https://img.shields.io/badge/Docker-Enabled-blue?logo=docker&logoColor=white)](https://www.docker.com/)
[![Kubernetes](https://img.shields.io/badge/Kubernetes-Ready-326CE5?logo=kubernetes&logoColor=white)](https://kubernetes.io/)
[![OpenShift](https://img.shields.io/badge/OpenShift-Supported-EE0000?logo=redhatopenshift&logoColor=white)](https://www.redhat.com/en/technologies/cloud-computing/openshift)

This project demonstrates how to containerize an **Object Detection (YOLOv5)** application and deploy it onto enterprise-grade container orchestration platforms like **Kubernetes** and **Red Hat OpenShift**.

---

## 🌟 Key Features
* **Real-time Detection:** Powered by YOLOv5 (Small variant) for high-speed inference.
* **Cloud-Native:** Fully Dockerized and ready for K8s/OpenShift clusters.
* **Automated Deployment:** Includes Shell scripts for one-click deployment and rolling updates.
* **Scalable:** Defined Kubernetes manifests for scaling pods based on demand.
* **Web Integration:** Flask/Python-based UI for visualizing detection results.

---

## 📂 Project Structure
* `kubernetes/` & `kubernetes-files/`: Contains YAML manifests for Deployments, Services, and Routes.
* `Dockerfile`: Instructions to build the YOLOv5 container image.
* `finalrun.py`: The main application script for detection and web serving.
* `deploy_script.sh`: Script to automate the deployment process.
* `rollingupdate.sh`: Handles zero-downtime updates for the application.

---

## 🛠️ Setup & Usage

### 1. Build the Docker Image
```bash
docker build -t your-username/yolov5-app:latest .
2. Run Locally
Bash
python finalrun.py
3. Deploy to Kubernetes/OpenShift
Make sure you are logged into your cluster (oc login or kubectl config), then run:

Bash
./deploy_script.sh
⚙️ Kubernetes Manifests
The application uses standard K8s objects:

Deployment: Manages the lifecycle of YOLOv5 pods.

Service: Provides a stable IP/DNS for the pods.

Route (OpenShift): Exposes the service to the external world.

🤝 Contributing
Feel free to open issues or submit pull requests to improve the deployment scripts or model integration.

Developed by Amarnath Mahato
