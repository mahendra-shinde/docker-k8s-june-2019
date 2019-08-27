## Demo3 : IIS Container 

1.  Pull new images

    ```shell
    $ docker pull mcr.microsoft.com/windows/servercore/iis:windowsservercore
    ```

2.  Launch a new container (Notice no entry-point after image name)

    ```shell
    $ docker run --name c01 -d mcr.microsoft.com/windows/servercore/iis:windowsservercore 
    ```

3.  View the list of running container, note the NAME of IIS container

    ```shell
    $ docker ps
    ```

4.  Get inside the container to retreive IP address for container "c01".

    ```shell
    $ docker exec -it c01 cmd
    $ ipconfig
    # Copy IP address and then QUIT
    $ exit
    ```

5.  Open web browser and visit IP address of container 
    You must be getting default IIS server welcome page.

6.  Now, Enter inside the container once again to create new welcome page.

    ```shell
    $ docker exec -it c01 powershell
    $ cd \inetpub\wwwroot
    $ set-content -Path index.htm -Value "<h2>Hello India</h2>"
    $ exit
    ```

7.  Refresh the browser page you have opened in step# 5.
    You should get Hello India this time.

8.  Capture this container and convert into an image.

    ```shell
    $ docker stop c01
    $ docker commit c01 mywebsite:1
    $ docker images
    ```

9.  Kill the old c01 and create new one using new image name.

    ```shell
    $ docker rm c01
    $ docker run -d --name c02 mywebsite:1 
    ```
10. Test IIS using container ip on web browser.
