✅ Understanding Volumes and Persistent Volume Claims (PVCs)
In Kubernetes, Volumes and Volume Claims are used to manage persistent storage, especially for stateful applications like databases, file uploads, or caching. Here's a breakdown:

🧱 Volumes
A Volume in Kubernetes is a directory accessible to containers in a Pod.

It is used to store data that should persist beyond the container lifecycle (e.g., when a container crashes or is restarted).

Volumes can be backed by different storage providers: hostPath (local disk), NFS, cloud storage, etc.

📄 Persistent Volume (PV)
A Persistent Volume is a piece of storage in the cluster that has been provisioned by an admin or dynamically by a StorageClass.

It is independent of any individual Pod and remains available even if the Pod dies.

🧾 Persistent Volume Claim (PVC)
A Persistent Volume Claim is a request for storage by a user.

Pods use PVCs to mount storage defined in a PV.

PVCs allow decoupling Pod and Storage: Pods declare the storage they need without knowing the details of the underlying storage.

🛠️ Adding a Volume & PVC to Your Deployment
Let’s assume you want to mount a directory inside the container (e.g., /app/data) for persistent logs or file storage. We’ll define:

- A PersistentVolume

- A PersistentVolumeClaim

- Reference the PVC in the Deployment


Note: Please substitute manifest file names where appropriate

| Action                        | Command                                                             |
| ----------------------------- | ------------------------------------------------------------------- |
| Apply a PersistentVolume      | `kubectl apply -f pv.yaml`                                          |
| Apply a PersistentVolumeClaim | `kubectl apply -f pvc.yaml`                                         |
| List all PVs                  | `kubectl get pv`                                                    |
| List all PVCs                 | `kubectl get pvc`                                                   |
| Describe a PV or PVC          | `kubectl describe pv <pv-name>` / `kubectl describe pvc <pvc-name>` |
| Delete PV or PVC              | `kubectl delete pv <pv-name>` / `kubectl delete pvc <pvc-name>`     |


