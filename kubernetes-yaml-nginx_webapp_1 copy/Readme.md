Create a deployment yaml using the command
kubectl create deployment nginx-webapp2 --image=vishwa787/webapp-2 --dry-run=client -o yaml > nginx-webapp2.yaml	

Test the deploymeny in K8s
kubectl apply -f nginx-webapp1.yaml

Create a service for accessing the webapp
kubectl create service nodeport nginx-webapp2-service --tcp=5679:80 --dry-run=client -o yaml