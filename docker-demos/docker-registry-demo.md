## Pushing an Image

1. Sign in on https://hub.docker.com
    Keep the docker hub page open in web browser.

2.  Open powershell or cmd and try following command:

    ```shell
    $ docker login
    Username: {your docker login}
    Password: {your password}
    ```

    NOTE:  Password won't echo back. rather no character like "*" would be displayed.
           It's possible to login without credentials if docker desktop has already
            linked to your docker account.


3.  Pull the sample image and TAG it with your dockerhub account.

    ```shell
    $ docker pull mcr.microsoft.com/windows/servercore/iis:windowsservercore  
    $ docker tag mcr.microsoft.com/windows/servercore/iis:windowsservercore  {yourdockeracc}/mysample-iis:1
    $ docker push {yourdockeracc}/mysample-iis:1
    ```

    NOTE: Replace {yourdockeracc} with actual docker account name.

4.  Refresh your web browser to verify the newly uploaded image repository.


