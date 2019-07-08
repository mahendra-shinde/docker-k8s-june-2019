## Docker STOP & Docker TOP

Launch a new container with PING command 

    $ docker run -it --name c2 mcr.microsoft.com/windows/servercore ping -t localhost

Open another command prompt, and check processes inside container c2

    $ docker top c2

Try to Stop it!

    $ docker stop c2

Delete the container

    $ docker rm c2


