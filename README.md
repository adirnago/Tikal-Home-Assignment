# Tikal-Home-Assignment
**Hands On:**
1. Create new redis-deployment.yaml file on your linux machine. 
2. Copy the content of Redis-Deployment & ConfigMaps file to the file from the privios step.
3. Run the command kubectl apply -f redis-deployment.yaml for applying the file
4. Check if the pod is running by the command - kubectl get pod
5. Exec into the pod by the command- kubectl exec -it redis-nae -- bin/sh
6. Verify that you can exec to the pod by - redis-cli
7. Check if the protected-mode is enable by the command -CONFIG GET protected-mode
8. Check if the loglevel is config to debug by the command -CONFIG GET loglevel

**Bonus:**
1. The first step is to installed the Helm client by this script:
$ curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/master/scripts/get-helm-3
$ chmod 700 get_helm.sh
$ ./get_helm.sh

Once you have Helm ready, you can add a chart repository by this command:
$ helm repo add URL
**for example:** helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx
and then do: helm repo update. for make sure we get the latest list of charts

The next step is to install a chart by the command: $ helm install bitnami/mysql --generate-name

2. Of course that my recommended redis helm is the official one with the name "prometheus-redis-exporter"
3. Helm Charts allow us to deploy the Redis Enterprise service using a single command to a Kubernetes namespace instead of deploy all the required Kubernetes resources manually
