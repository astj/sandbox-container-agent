# sandbox

secret

```
export MACKEREL_APIKEY=...
kubectl create secret generic mackerel-container-agent --from-literal "MACKEREL_APIKEY=${MACKEREL_APIKEY}"
```

deploy

```
export IMAGE_NAME=mackerel/mackerel-container-agent:latest
cat pod.yml | envsubst | kubectl apply -f -
```

ekstl

```
export AWS_PROFILE=...
eksctl create cluster -f eksctl.yml
```

You might need some hacks when MFA enabled for AWS:
```
FILE=$(mktemp); cat pod_eks.yml | envsubst > $FILE; kubectl apply -f $FILE; rm $FILE
```
