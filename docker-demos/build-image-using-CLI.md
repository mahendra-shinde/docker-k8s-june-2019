### Using Command line 

1. Pull base image
```cmd
$ docker pull mcr.microsoft.com/windows/servercore/iis
```

2. Create a temporary container
```cmd
$ docker run --name temp1 -it mcr.microsoft.com/windows/servercore/iis powershell
```

3. Enter inside temporary container and execute few commands

```cmd
$ docker exec -it temp1 powershell
$ cd inetpub\wwwroot
$ del *.htm
$ mkdir \myapp
$ exit
```
    
4. Copy your files/application

    Open a new command prompt or powershell windows
    Switch to folder which contains your application. use following command to copy files

```cmd
$ docker cp c:\myapp\*.html temp1:\myapp
```

5. Test the application

    Use Container's IP address to test the application deployment.

6   Stop the container

```cmd
$ docker stop temp1
 ```

7  Capture the container's state into a new image.

```cmd
$ docker commit -t myapp:1 temp1
```

8  Delete the temporary container

```cmd
$ docker rm temp1
```
