# Kubernetes

# Kubernetes Service (Deep Dive)
## There are three types of services in k8s
1. Cluster IP Mode
2. NodePort Mode
3. Load Balancer Mode

## Cluster IP Mode:
  1. First create deployment.yml file
  2. Delpoy a yaml file into the cluster  --> kubectl apply -f deployment.yml  --> kubectl get deploy  --> kubectl get pods   --> kubectl get -o wide   --> kubectl get pods -v=7/9
  3. Need to chekc this by using:  minikube ssh  --> curl https://IP address of pods
  4. This mode will access within the cluster

## NodePort Mode:
  1. First create service.yml file
  2. Delpoy a yaml file into the cluster  --> kubectl apply -f service.yml (note: use same label/selector)  --> kubectl get svc  --> kubectl get svc -v=7/9
  3.  Need to chekc this by using:  minikube ssh  --> curl https://IP address of svc (within cluster)
  4.  We can access this by usng NodePort -->curl http://IP address:Portnumber (note: those who have this Ip address cqn access this application)
