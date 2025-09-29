# Kubernetes App Deployment on Windows

## Objective
Deploy and manage applications in Kubernetes using Minikube, kubectl, and Docker.

## Tools Used
- Minikube
- kubectl
- Docker Desktop
- YAML files for deployment and service

## Steps Performed
1. **Setup Tools**
   - Installed Docker Desktop, Minikube, and kubectl on Windows.
2. **Start Minikube Cluster**
   - `minikube start --driver=docker --memory=3584 --cpus=2`
3. **Create Deployment**
   - Defined `deployment.yaml` for Nginx app with replicas.
   - Applied using `kubectl apply -f deployment.yaml`.
4. **Expose App via Service**
   - Created `service.yaml` with NodePort.
   - Applied using `kubectl apply -f service.yaml`.
   - Accessed service using `minikube service myapp-service --url`.
5. **Manage Deployment**
   - Scaled pods: `kubectl scale deployment myapp-deployment --replicas=4`
   - Checked logs: `kubectl logs <pod-name>`
   - Described deployment: `kubectl describe deployment myapp-deployment`
6. **Optional**
   - Used Minikube dashboard: `minikube dashboard`

## Deliverables
- `deployment.yaml`
- `service.yaml`
- Screenshots of pods, services, and app running

## Notes
This project demonstrates basic Kubernetes deployment management on a Windows machine.
