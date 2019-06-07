## Rolling Updates

1. Make sure the deployment exists!

    $ kubectl apply -f 03-deployment.yml
    
2.  List all Replica Sets

    $ kubectl get rs 

3.  Open "03-deployment.yml" file and change the image name.
    replace nginx:1.10 to nginx:1.7.9
    Save and Close the file

4.  Trigger rolling update by simply using following command:

    $ kubectl apply -f 03-deployment.yml

5.  Check Status of Rolling update:

    $ kubectl rollout status deploy deployment-example

6.  Rolling Update history:
    $ kubectl rollout history deploy deployment-example

7.  Check the replica Sets

    $ kubectl get rs

8.  Undo last update

    $ kubectl rollout undo deploy deployment-example
