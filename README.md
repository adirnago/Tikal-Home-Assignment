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
$ helm repo add + URL
**for example:** helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx
and then do: helm repo update. for make sure we get the latest list of charts

The next step is to install a chart by the command: $ helm install bitnami/mysql --generate-name

2. Of course that my recommended redis helm is the official one with the name "prometheus-redis-exporter", because of the reason that it is oddicial and verified publisher.
In addition, new versions often comes out and his security level is high.

3. 

**CI-CD with Github Actions:**
1. Create a new file in the .github/workflows
2. Clone the git repository to your linux machine
3. Copy the following YAML contents into the test.yml file under test/spring-petclinic/.github/workflows:
name: GitHub Actions Demo
on: [push]
jobs:
  Explore-GitHub-Actions:
    runs-on: ubuntu-latest
    steps:
      - run: echo "🎉 The job was automatically triggered by a ${{ github.event_name }} event."
      - run: echo "🐧 This job is now running on a ${{ runner.os }} server hosted by GitHub!"
      - run: echo "🔎 The name of your branch is ${{ github.ref }} and your repository is ${{ github.repository }}."
      - name: Check out repository code
        uses: actions/checkout@v2
      - run: echo "💡 The ${{ github.repository }} repository has been cloned to the runner."
      - run: echo "🖥️ The workflow is now ready to test your code on the runner."
      - name: List files in the repository
        run: |
          ls ${{ github.workspace }}
      - run: echo "🍏 This job's status is ${{ job.status }}."
4. git add-> git commit -> git push
![image](https://user-images.githubusercontent.com/53764172/125198699-b4f0f380-e26b-11eb-85f2-c41a321b4c0c.png)

**Bonus:**
1. Sign up on Code Inspector.
2. In your profile, generate API keys.
3. On GitHub, go in your repository settings, click on the Secrets  and create a new secret with the value of the access key generated at the previous step
(Pay attention, you need two secrets, one for SECRET_KEY and one for ACCESS_KEY)
4. Create a file .github/workflows/main.yml and insert the following content (take it from main.yml file)

![image](https://user-images.githubusercontent.com/53764172/125200967-db1b9100-e275-11eb-9d62-79daa02a920d.png)

