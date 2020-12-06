# image-syncer

Sync k8s.gcr.io docker images to dockerhub use [aliyun image-syncer](https://github.com/AliyunContainerService/image-syncer)


If you want list repository or image tag, Open [google cloudshell](https://console.cloud.google.com/cloudshell) and run:

```
gcloud container images list --repository=k8s.gcr.io/metrics-server
gcloud container images list-tags k8s.gcr.io/metrics-server/metrics-server
```
