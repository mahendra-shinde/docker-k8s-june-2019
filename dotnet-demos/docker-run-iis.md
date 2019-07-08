Launch new IIS container

    $ docker run -d --name c3 mcr.microsoft.com/windows/servercore/iis:windowsservercore-ltsc2016

Get the PRIVATE IP address of Container

    $ docker inspect c3

    OR Short form

    $ docker inspect --format "{{.NetworkSettings.Networks.nat.IPAddress }}"  c3


Now, Open web browser enter address : http://{IPADDRESS}/


Now, Enter inside running container

    $ docker exec -it c3 cmd

Goto inetput/wwwroot directory 
    
    $ cd inetput/wwwroot

Replace iisstart.htm with custom page

    $ del iisstart.htm
    $ echo "<h2> Hello World</h2>" > iisstart.htm

Stop but DONT DELETE
    
    $ docker stop c3

Commit the changes into NEW image

    $ docker commit c3 myapp:1

Try creating new container from new image
    
    $ docker run -d --name c4 myapp:1

Clean Up

    $ docker stop c3 c4
    $ docker rm c3 c4