# kubernetes scripts and configurations

## apply changes to minicube
kubectl apply -f <foldercontaining k8s files>
## applying a single file to minikube
kubectl apply -f <filename.yaml> 
## to check for deploments in the minikube
kubectl get deplopments
## to check serives
kubectl get services
## to check pods
kubectl get pods
## createing secretes in k8s -password
kubectl create secret generic pgpassword --from-literal PGPASSWORD=chantos7
## verify if the secrets are saved
kubectl get secrets
## to delete a config
kubectl delete -f <filename.yaml>
## to delete a deployment
kubectl delete deployment <deploymentname>
## to delete a service
kubectl delete service <servicename>
## to update a deployment
## first tag the new image and push it to docker hub the use the new inage with the tag
kubectl set image deployment/client-deployment client=myrachanto/ddd:v5
