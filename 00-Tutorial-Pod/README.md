🔹 What is a Pod?
A Pod is the smallest deployable unit in Kubernetes. It represents a single instance of a running process in your cluster.

You can think of a Pod as a wrapper around one or more containers (usually one), with shared resources like storage, network, and configuration.

📌 Why use Pods?
Encapsulates one or more tightly coupled containers.

Ensures containers inside a pod can communicate via localhost.

Shares storage volumes and network IP.

Ideal when two containers must run together (e.g., app + sidecar).

Note: Please substitute manifest file names where appropriate

| Action                         | Command                                    |
| ------------------------------ | ------------------------------------------ |
| Create a pod                   | `kubectl apply -f pod.yaml`                |
| List all pods                  | `kubectl get pods`                         |
| Get detailed info              | `kubectl describe pod <pod-name>`          |
| View logs                      | `kubectl logs <pod-name>`                  |
| Execute a command inside a pod | `kubectl exec -it <pod-name> -- /bin/bash` |
| Delete a pod                   | `kubectl delete pod <pod-name>`            |
