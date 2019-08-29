## Config Map Demo

1. Create a configmap from file [mysecret2](./mysecret2.yaml)

    ```shell
    $ kubectl apply -f ./mysecret2.yaml
    $ kubectl describe -f ./mysecret2.yaml
    ```

2.  Create a pod that uses secret [pod](./pod-3B.yaml)

    ```shell
    $ kubectl apply -f ./pod-3B.yaml
    $ kubectl get pods
    ```

3.  Once, pod status for "pod3b" chages to RUNNING,
    try entering inside the pod.

    ```shell
    $ kubectl exec pod3b -it sh  
    $ echo $MYSQL_USER
    $ echo $MYSQL_PASSWORD
    ```

4.  Delete the resources

    ```shell
    $ kubectl delete -f pod-3B.yaml
    $ kubectl delete -f mysecret2.yaml
    ```