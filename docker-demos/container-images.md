## Container Images
mcr.microsoft.com/windows/servercore/iis:windowsservercore

### mcr.microsoft.com/   

    Registry URL, this registry is PUBLIC registry maintained by Microsoft with Read Only access to General Public

### windows/servercore/

    Group of Container repositories 

### iis

    Image repository. Collection of multiple version of same image.
    Must contain AT LEAST ONE container image.

### :windowsservercore

    Individual container image from 'iis' repository.
    default name is "latest"
    Also called TAG

## Assigning a new image name (TAG) to existing image

    Syntax: docker tag {OLD-NAME} {NEW-NAME}
    ```shell
    $  docker tag mcr.microsoft.com/windows/servercore/iis:windowsservercore iis        
    ```

> NOTE: Old-name still exists!
>      image names must be in lowercase, and doen't allow spaces.
>      may use underscore or hyphen.