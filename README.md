## image-syncer

Sync k8s.gcr.io docker images to dockerhub use [aliyun image-syncer](https://github.com/AliyunContainerService/image-syncer) + githubAction


If you want list repository or image tag, Open [google cloudshell](https://console.cloud.google.com/cloudshell) and run:

```
gcloud container images list --repository=k8s.gcr.io/metrics-server
gcloud container images list-tags k8s.gcr.io/metrics-server/metrics-server
```

## Getting Started

1、fork this repo, then create your self secrets:
```
Settings-->Secrets-->New Repository Secrets--> Add your DOCKERHUB_USERNAME and DOCKERHUB_PASSWORD key values.
```

2、add registry to `images:` that you want to sync:

```yaml
auth:
  registry.hub.docker.com:
    username: USERNAME
    password: PASSWORD
images:
  k8s.gcr.io/metrics-server/metrics-server: willdockerhub/metrics-server
  k8s.gcr.io/ingress-nginx/controller: willdockerhub/ingress-nginx-controller
  k8s.gcr.io/git-sync/git-sync: willdockerhub/git-sync
  gcr.io/kaniko-project/executor:debug,latest: willdockerhub/kaniko-executor
  k8s.gcr.io/kube-state-metrics/kube-state-metrics: willdockerhub/kube-state-metrics
  k8s.gcr.io/sig-storage/nfs-subdir-external-provisioner: willdockerhub/nfs-subdir-external-provisioner
  k8s.gcr.io/prometheus-adapter/prometheus-adapter: willdockerhub/prometheus-adapter
```

finished!


