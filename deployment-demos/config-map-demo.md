## Config Map Demo

1. Create a configmap from file [myconfig](./myconfig.yml)

    ```shell
    $ kubectl apply -f ./myconfig.yml
    $ kubectl describe -f ./myconfig.yml
    ```

2.  Create a pod that uses ConfigMap [pod](./pod-3.yaml)

    ```shell
    $ kubectl apply -f ./pod-3.yaml
    $ kubectl get pods
    ```

3.  Once, pod status for "pod3" chages to RUNNING,
    try entering inside the pod.

    ```shell
    $ kubectl exec pod3 -it sh  
    $ echo $MYSQL_USER
    $ echo $MYSQL_PASSWORD
    ```

4.  Delete the resources

    ```shell
    $ kubectl delete -f pod-3.yaml
    $ kubectl delete -f myconfig.yml
    ```