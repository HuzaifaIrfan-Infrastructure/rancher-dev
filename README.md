# rancher-dev

## Rancher Install

```sh
docker run -d --restart=unless-stopped -p 9090:80 -p 9091:443 --privileged -v /opt/rancher:/var/lib/rancher --name=rancher-dev rancher/rancher:v2.11.1-rc2-amd64
```

## Racher Kubernetes Agent


## Helm Install

```sh
kubectl get secret --namespace cattle-system bootstrap-secret -o go-template='{{.data.bootstrapPassword|base64decode}}{{"\n"}}'
```