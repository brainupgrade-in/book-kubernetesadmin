# book-kubernetesadmin

## Metal LB 
kubectl apply -f https://raw.githubusercontent.com/metallb/metallb/v0.13.7/config/manifests/metallb-native.yaml
kubectl apply -f https://raw.githubusercontent.com/brainupgrade-in/book-kubernetesadmin/main/chapter_04/metallb-config.yaml

## NGINX Ingress Controller
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/main/deploy/static/provider/kind/deploy.yaml

## Expose app to the internet
kubectl create ingress hello --rule="hello.brainupgrade.in/?(.*)=hello:80" --class nginx

## How to find out eth0 address of current host
ip addr show eth0 | grep "inet\b" | awk '{print $2}' | cut -d/ -f1