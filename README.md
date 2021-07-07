# Tikal-Home-Assignment
1. Create new redis-deployment.yaml file on your linux machine. 
2. Copy the content of Redis-Deployment & ConfigMaps file to the file from the privios step.
3. Run the command kubectl apply -f redis-deployment.yaml for applying the file
4. Check if the pod is running by the command - kubectl get pod
5. Exec into the pod by the command- kubectl exec -it redis-nae -- bin/sh
6. Verify that you can exec to the pod by - redis-cli
7. Check if the protected-mode is enable by the command -CONFIG GET protected-mode
8. Check if the loglevel is config to debug by the command -CONFIG GET loglevel
