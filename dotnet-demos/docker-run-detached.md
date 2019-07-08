## Run container in detached mode / daemon mode

Run a new container in detached mode

    $ docker run -d --name c2 9c52 ping -t localhost

Get the static output / LOG from container
    
    $ docker logs c2

Remove & Stop

    $ docker stop c2
    $ docker rm c2
