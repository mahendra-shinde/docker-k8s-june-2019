## Working with Volumes

1. Create a new named Volume

    ```shell
    $ docker volume create vol1
    ```

2.  Create a new container and assign this volume at c:/folder1 path
    NOTE: 'env-test' is container images which has 'folder1' created at C:\

    ```shell
    $ docker run -it  --name cn1 --mount source=vol1,target="C:/folder1"   env-test cmd           
    $ cd /folder1
    $ echo "Hello India" > file1
    $ exit
    ```

3.  Create another container with same volume.

    ```shell
    $ docker run --name cn2 -it -v vol1:"c:/folder1" env-test cmd     
    $ cd folder1
    $ type file1
    $ echo "The quick brown fox jumps over the lazy dog" > file1
    $ exit
    ```

4.  Switch back to cn1 (First container)

    ```shell
    $ docker exec -it cn1 cmd
    $ cd folder1
    $ type file1
    $ exit
    ```