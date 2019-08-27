## Docker Networks

1. List all existing container Networks
    ```shell
    $ docker network ls
    ```

2.  Create a new container network 

    ```shell
    $ docker network create -d transparent --subnet 180.18.0.0/24 net1  
    ```

3.  Verify the network configuration

    ```shell
    $ docker inspect net1
    ```

4.  Launch a web application container

    ```shell
    $ docker run -d --network net1 --name cn03 --hostname webapp myaspapp:1   
    $ docker inspect cn03
    ```

5.  Now, if you try accessing application from browser using container-ip, it would fail!

6.  Launch a basic powershell container

    ```shell
    $ docker run -it --name cn01 --network net1 --hostname container1 env-test powershell
    $ invoke-webrequest -UseBasicParsing -Uri http://webapp
    $ ping webapp
    $ exit
    ```