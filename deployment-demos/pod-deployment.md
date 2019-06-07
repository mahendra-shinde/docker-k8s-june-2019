## Command to deploy 
$ kubectl apply -f pod-1.yaml

## Command to list pods
$ kubectl describe -f pod-1.yaml
OR
$ kubectl describe pods pod1

## Delete earlier deployment
$ kubectl delete pods pod1
OR
$ kubectl delete -f pod-1.yaml

## Get Container LOGS
$ kubectl logs pod1 web
$ kubectl logs pod1 db