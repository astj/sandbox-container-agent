# sandbox

deploy

```
export MACKEREL_APIKEY=...
export IMAGE_NAME=mackerel/mackerel-container-agent:latest
cat pod.yml | envsubst | kubectl apply -f -
```
