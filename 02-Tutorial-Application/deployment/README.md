Deployment
Purpose: A Deployment provides declarative updates to pods and ReplicaSets. It allows you to manage pod versions, perform rolling updates, rollbacks, and ensure that the right number of pods are running. A Deployment creates and manages a ReplicaSet behind the scenes to control the scaling and updates of pods.

Key Features:

Manages the lifecycle of a ReplicaSet.

Supports rolling updates to deploy new versions of applications with zero downtime.

Provides version control, rollback, and scaling options.

Supports continuous integration/deployment (CI/CD) pipelines.

Limitations:

Deployments are not well-suited for scenarios where fine-grained control over individual pod configurations is needed (i.e., for non-stateless applications).

Note: Please substitute manifest file names where appropriate

| Action                          | Command                                                       |
| ------------------------------- | ------------------------------------------------------------- |
| Create a Deployment             | `kubectl apply -f deployment.yaml`                            |
| List all Deployments            | `kubectl get deployments` or `kubectl get deploy`             |
| Get detailed info               | `kubectl describe deployment <deployment-name>`               |
| Update deployment (e.g., image) | `kubectl set image deployment/<name> <container>=<new-image>` |
| Scale a deployment              | `kubectl scale deployment <deployment-name> --replicas=5`     |
| Rollback to previous revision   | `kubectl rollout undo deployment <deployment-name>`           |
| Delete a deployment             | `kubectl delete deployment <deployment-name>`                 |
