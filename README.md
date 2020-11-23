# metrics-server docker images

sync k8s.gcr.io/metrics-server/metrics-server docker images to dockerhub.


open [google cloudshell](https://console.cloud.google.com/cloudshell) and run:

```
gcloud container images list --repository=k8s.gcr.io/metrics-server
gcloud container images list-tags k8s.gcr.io/metrics-server/metrics-server
```
