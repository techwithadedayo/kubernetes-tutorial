🔹 What is a Service?
A Service in Kubernetes is a logical abstraction that defines a policy to access a set of Pods. It provides a stable IP address and DNS name, even as pods are replaced or scaled.

📌 Why use Services?
Pods have dynamic IPs — Services provide stable networking.

Enables load balancing between multiple pod replicas.

Decouples client apps from pod details.

Note: Please substitute manifest file names where appropriate

| Action                            | Command                                     |
| --------------------------------- | ------------------------------------------- |
| Create a service                  | `kubectl apply -f service.yaml`             |
| List all services                 | `kubectl get services` or `kubectl get svc` |
| Get details of a service          | `kubectl describe service <service-name>`   |
| Access NodePort service (locally) | `minikube service <service-name> --url`           |
| Delete a service                  | `kubectl delete service <service-name>`     |
