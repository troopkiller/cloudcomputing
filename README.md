kubectl create namespace kuma

kubectl apply -f .\kuma-db.yaml 
kubectl apply -f .\kuma-svc.yaml 
kubectl apply -f .\kuma-ingress.yaml 
kubectl apply -f .\kuma-pvc.yaml 

kubectl delete -f .\kuma-db.yaml  
kubectl delete -f .\kuma-svc.yaml 
kubectl delete -f .\kuma-ingress.yaml 
kubectl delete -f .\kuma-pvc.yaml 

kubectl get all -n uptime-kuma
kubectl logs <pod-name> -n uptime-kuma
kubectl port-forward service/kuma 3001:3001 -n kuma
