# squid-helm
helm repo for squid proxy servers


docker image: https://hub.docker.com/r/ubuntu/squid

## Deploy with Kubernetes
Works with any Kubernetes; if you don't have one, we recommend you install MicroK8s⁠ and microk8s.enable dns storage then snap alias microk8s.kubectl kubectl.

Download squid.conf⁠ and squid-deployment.yml⁠ and set containers.squid.image in squid-deployment.yml to your chosen channel tag (e.g. ubuntu/squid:5.2-22.04_beta), then:

```
kubectl create configmap squid-config --from-file=squid=squid.conf
kubectl apply -f squid-deployment.yml
```
You can now access the squid proxy on port 3128
