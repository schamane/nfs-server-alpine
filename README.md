# NFS Server for kubernetes based on alpine


## NFS Server Container

ref:

[matthewpalmers blog article](https://matthewpalmer.net/kubernetes-app-developer/articles/kubernetes-volumes-example-nfs-persistent-volume.html)

Docker image to create smallest possible docker image

## Helm chart

### Add Repo

Add repo to local helm repos

```bash
helm repo add nfs-server-alpine https://schamane.github.io/nfs-server-alpine
```

### Use Helmet Chart

You will need to have PVC first, than deploy chart

```bash
helm -n <namespace> install -f values.yaml nfs-server-alpine nfs-server-alpine/nfs-server-alpine
```