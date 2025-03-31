# Squid Helm Chart
## Squid | Ubuntu
Current Squid Docker Image from Canonical⁠, based on Ubuntu. Receives security updates and rolls to newer Squid or Ubuntu release. This repository is free to use and exempted from per-user rate limits.

## About Squid
Squid is a caching proxy for the Web supporting HTTP, HTTPS, FTP, and more. It reduces bandwidth and improves response times by caching and reusing frequently-requested web pages. Squid has extensive access controls and makes a great server accelerator. It runs on most available operating systems, including Windows and is licensed under the GNU GPL.


## Deploy with Kubernetes
Works with any Kubernetes; if you don't have one, we recommend you install MicroK8s⁠ and microk8s.enable dns storage then snap alias microk8s.kubectl kubectl.

Download squid.conf⁠ and squid-deployment.yml⁠ and set containers.squid.image in squid-deployment.yml to your chosen channel tag (e.g. ubuntu/squid:5.2-22.04_beta), then:

```
kubectl create configmap squid-config --from-file=squid=squid.conf
kubectl apply -f squid-deployment.yml
```
You can now access the squid proxy on port 3128