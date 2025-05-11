Step 1

kubectl apply -f apps-pod-node.yaml

Step 2: To see the pod and the service

kubectl get all


Step 3: Check the logs of the app
kubectl logs -f my-app


step 5: exec into the container to check
kubectl exec -it my-app -- sh


Step 5: do ls and install curl

ls
apk add curl

Step 6: Run command from inside pod to see if it works:

 curl -X POST http://localhost:5000/api/auth/register \
  -H "Content-Type: application/json" \
  -d '{"email":"bosun@example.com","password":"123456"}'

Step 7: Navigate to the minikube service URL

minikube service my-app-service --url



