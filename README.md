## Getting Started

1、fork this repo, then create your self secrets:
```
Settings-->Secrets-->New Repository Secrets--> Add your DOCKERHUB_USERNAME and DOCKERHUB_PASSWORD key values.
```
![githubaction01.png](https://i.loli.net/2021/08/21/TjN76FtngG5Dehf.png)

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

3、check action logs

![githubaction02.png](https://i.loli.net/2021/08/21/OkXVWY8pN6Foat7.png)

4、check your images, congratulations!

dockerhub

![githubaction03.png](https://i.loli.net/2021/08/21/K2PzDTV3qu61WIO.png)

aliyun

![githubaction04.png](https://i.loli.net/2021/08/21/drQzkbeCNDXqcH4.png)


