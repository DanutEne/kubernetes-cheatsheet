1. install hyperhit and minikube
```
brew update
brew install hyperkit
brew install minikube
kubectl
minikube
```

2. create minikube cluster
```
minikube start --vm-driver=hyperkit
kubectl get nodes
minikube status
kubectl version
```

3. delete cluster and restart in debug mode
```
minikube delete
minikube start --vm-driver=hyperkit --v=7 --alsologtostderr
minikube status
```

4. kubectl commands
```
kubectl get nodes
kubectl get pod
kubectl get services
kubectl create deployment nginx-depl --image=nginx
kubectl get deployment
kubectl get replicaset
kubectl edit deployment nginx-depl
```

5. debugging
```
kubectl logs {pod-name}
kubectl exec -it {pod-name} -- bin/bash
```

6. create mongo deployment
```
kubectl create deployment mongo-depl --image=mongo
kubectl logs mongo-depl-{pod-name}
kubectl describe pod mongo-depl-{pod-name}
```

7. delete deplyoment
```
kubectl delete deployment mongo-depl
kubectl delete deployment nginx-depl
```

8. create or edit config file
```
vim nginx-deployment.yaml
kubectl apply -f nginx-deployment.yaml
kubectl get pod
kubectl get deployment
```

9. delete with config
```
kubectl delete -f nginx-deployment.yaml
```

#Metrics
```
kubectl top
```
The kubectl top command returns current CPU and memory usage for a cluster’s pods or nodes, or for a particular pod or node if specified.
