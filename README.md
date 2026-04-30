# 🚀 Kubernetes Monitoring with Prometheus & Grafana

## 📌 Project Overview
This project demonstrates how to monitor a Kubernetes cluster using Prometheus and Grafana.

## 🧱 Architecture
Kubernetes → Node Exporter → Prometheus → Grafana

## ⚙️ Setup Steps

### 1. Create Namespace
kubectl apply -f manifests/namespace.yaml

### 2. Deploy Node Exporter
kubectl apply -f manifests/node-exporter-daemonset.yaml

### 3. Install Prometheus (Helm)
helm install prometheus prometheus-community/kube-prometheus-stack -n monitoring

### 4. Access Grafana
kubectl port-forward svc/prometheus-grafana -n monitoring 3000:80

## 📊 Dashboard
Grafana Dashboard ID: 1860

## 📁 Project Structure
- manifests/ → Kubernetes YAML files
- screenshots/ → Dashboard images
- docs/ → Architecture diagrams

## 👨‍💻 Author
Hema Sri Chandika
