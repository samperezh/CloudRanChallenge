# CloudRanChallenge

## Instructions
1. Using minikube or Docker Desktop create a Kubernetes environment, you can also choose any available infrastructure such as Katacoda.
2. Deploy hello app gcr.io/google-samples/hello-app:2.0 to your cluster. Source hello app
3. Expose the service and test it with the curl request: curl http://<ip address of exposed service>:8080.
4. Once everything is working, push your project yml files to your github repository. You would need to share the link to the github project by the end of the test.
5. Package your application with Helm.
6. Redeploy your hello app using Helm chart.
7. Push your helm chart to github and share the project link.

## Part 1: K8s Deployment yml files
To deploy and expose hello app using the K8s Deployment yml files directly run the following commands from CloudRanChallenge/k8syml/:
1. minikube start 
2. kubectl apply -f deployment.yml
3. kubectl apply -f service.yml

As my minikube uses Docker Desktop as driver, from new window run and it should output http:://X: 
4. minikube service hello-app-service --url

Back to original window run, test service: 
5. curl X

## Part 2: Package and Redeploy hello app using Helm chart
To deploy and expose hello app using the Helm chart run the following commands from CloudRanChallenge/buildachart/:
1. minikube start 
2. helm install my-chart .

As my minikube uses Docker Desktop as driver, from new window run and it should output http:://X: 
4. minikube service buildachart-svc --url

Back to original window run, test service: 
5. curl X