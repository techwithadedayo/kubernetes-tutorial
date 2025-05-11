1. ReplicaSet
Purpose: A ReplicaSet ensures that a specified number of identical pod replicas are running at any given time. If a pod fails or is deleted, the ReplicaSet will create a new pod to maintain the specified number of replicas.

Key Features:

Ensures high availability by running a set of identical pods.

Manages the scaling of pods (up or down).

Does not handle upgrades or rolling updates of the pods.

Limitations:

ReplicaSets only manage replicas and cannot control the versioning or upgrades of the pods. They don’t provide declarative updates to the pod configurations.

You cannot manage deployment lifecycle events like rolling updates, rollbacks, or version management directly with ReplicaSets.


Note: Please substitute manifest file names where appropriate

| Action              | Command                                 |
| ------------------- | --------------------------------------- |
| Create a ReplicaSet | `kubectl apply -f replicaset.yaml`      |
| List ReplicaSets    | `kubectl get rs`                        |
| Describe ReplicaSet | `kubectl describe rs <replicaset-name>` |
| Delete ReplicaSet   | `kubectl delete rs <replicaset-name>`   |


#Pods and Replicasets are loosley coupled.
# this will delete the rs and the pods will become orphans with no self healing and no autoscaling capabilities.
kubectl delete rs my-app-replicaset --cascade=orphan