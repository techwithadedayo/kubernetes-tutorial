🔷 1. ConfigMap — Explanation
ConfigMap is used to store non-sensitive configuration data (like environment variables, settings, or file contents) that your app might need.

✅ Use cases:
Database connection strings (without passwords)

Application settings or flags

External config files

Note: Please substitute manifest file names where appropriate

| Action              | Command                                                       |
| ------------------- | ------------------------------------------------------------- |
| Create from file    | `kubectl create configmap my-config --from-file=config.txt`   |
| Create from literal | `kubectl create configmap my-config --from-literal=key=value` |
| Apply YAML          | `kubectl apply -f configmap.yaml`                             |
| View all ConfigMaps | `kubectl get configmap`                                       |
| View details        | `kubectl describe configmap <configmap-name>`                 |
| Delete a ConfigMap  | `kubectl delete configmap <configmap-name>`                   |




🔶 2. Secret — Explanation
Secret is used to store sensitive data such as passwords, tokens, or keys. Unlike ConfigMaps, values are base64 encoded.

✅ Use cases:
API keys

Database passwords

JWT secrets
Note: Please substitute manifest file names where appropriate

| Action                                  | Command                                                                 |                   |
| --------------------------------------- | ----------------------------------------------------------------------- | ----------------- |
| Create from literal                     | `kubectl create secret generic my-secret --from-literal=password=12345` |                   |
| Create from file                        | `kubectl create secret generic my-secret --from-file=secret.txt`        |                   |
| Apply YAML                              | `kubectl apply -f secret.yaml`                                          |                   |
| View Secrets (names only)               | `kubectl get secrets`                                                   |                   |
| Describe Secret (decoded base64 values) | `kubectl describe secret <secret-name>`                                 |                   |
| Decode a specific value                 | \`kubectl get secret <secret-name> -o jsonpath="{.data.<key>}"          | base64 --decode\` |
| Delete a secret                         | `kubectl delete secret <secret-name>`                                   |                   |

