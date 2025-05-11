 ✅ Step-by-Step Minikube Installation (Using Docker Driver)

 1. Install kubectl

Minikube needs kubectl to manage the cluster.

 macOS:

  ## bash  ##
  brew install kubectl
  

 Windows (PowerShell):

  ## powershell ##
  choco install kubernetes-cli
  

 2. Install minikube

 macOS (Homebrew):

  ## bash ##
  brew install minikube
  

 Windows (Chocolatey):

  ## powershell ##
  choco install minikube
  
 Linux 

   curl -LO https://github.com/kubernetes/minikube/releases/latest/download/minikube-linux-amd64
   sudo install minikube-linux-amd64 /usr/local/bin/minikube && rm minikube-linux-amd64

 3. Start Minikube with Docker driver

Make sure Docker Desktop is running, then:

## bash ##
minikube start --driver=docker


This will spin up a local Kubernetes cluster using Docker containers as nodes — very lightweight and efficient.

---

 🔍 Verify Installation

## bash  ##
minikube status
kubectl get nodes


You should see a running node in the Ready state.

---

 ⚙️ Optional: Enable Dashboard

## bash ##
minikube dashboard


This opens the Kubernetes dashboard in your browser.

---

 🧼 Stop / Delete Cluster (when needed)

## bash ##
minikube stop
minikube delete

