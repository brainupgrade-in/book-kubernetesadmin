# book-kubernetesadmin

## Metal LB 
kubectl apply -f https://raw.githubusercontent.com/metallb/metallb/v0.13.7/config/manifests/metallb-native.yaml
kubectl apply -f https://raw.githubusercontent.com/brainupgrade-in/book-kubernetesadmin/main/chapter_04/metallb-config.yaml

## NGINX Ingress Controller
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/main/deploy/static/provider/kind/deploy.yaml