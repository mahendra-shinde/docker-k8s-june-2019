## Service Demo
1. Deploy the [Deployment](./deployment-1.yaml)

    ```shell
    $ kubectl apply -f ./deployment-1.yaml 
    $ kubectl get rs -l name:myapp
    $ kubectl get po -l name:myapp
    ```

2.  Deploy the [Service](./service2.yml)

    ```shell
    $ kubectl apply -f ./service2.yml
    $ kubectl get svc myapp2
    ```

3.  Once all pods are UP and RUNNING, Visit following web url:

    http://localhost:30002