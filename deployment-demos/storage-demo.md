# Use Persistent Storage

1. Create PersistentVolume using [mydbvol](./my-pv.yml)

    ```shell
    $ kubectl apply -f my-pv.yml
    $ kubectl get pv
    ```

2.  Create PV Claim using [mypvc1](./my-pvc.yml)

    ```shell
    $ kubectl apply -f my-pvc.yml
    $ kubectl get pvc
    $ kubectl get pv
    ```
    Both pv and pvc must be BOUND to each other.

3.  Create a pod that request storage [pod5](./pod-volumeClaim.yaml) 

    ```shell
    $ kubectl apply -f pod-volumeClaim.yaml
    $ kubectl get pvc
    ```

