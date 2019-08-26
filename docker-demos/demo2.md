## Demo2 : Run, Start and  Stop Container

1.  Run a container to PING itself

    ```shell
    $ docker run mcr.microsoft.com/windows/servercore:ltsc2016 ping localhost
    ```

2.  Notice, Container would print few lines and it would QUIT

3.  Verify the status and view logs

    ```shell
    $ docker ps -a
    $ docker logs {CONTAINERID}
    ```

4.  Launch new container in DETACHED mode

    ```shell
    $ docker run --name c2 -d  mcr.microsoft.com/windows/servercore:ltsc2016 ping -t localhost 
    ```

    This container would continue to run unless we stop it manually.

5.  View the logs

    ```shell
    $ docker logs c2
    ```

6.  Stop the container and delete

    ```shell
    $ docker stop c2
    $ docker rm c2
    ```

7.  Enter inside running container with temp process

    ```shell
    $ docker exec -it wonderful_herschel cmd
    $ ipconfig
    $ exit
    ```