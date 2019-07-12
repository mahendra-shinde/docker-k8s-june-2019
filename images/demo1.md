## Create new Container and creating files

List all available images?
$ docker images

Pull nanoserver image (If Image not available)
$ docker pull mcr.microsoft.com/windows/servercore:ltsc2016

Create and Run new Container
$ docker run -it --name c1 mcr.microsoft.com/windows/servercore:ltsc2016 cmd

Where:
    docker run          Create and Start new Container
    -it                 -i Interactive, -t terminal
    IMAGE-name          Image to be used
    cmd                 Terminal Or Command to be used
                        Linux : bash or sh
                        Windows : cmd or powershell
    --name c1           User defined name for container

Create file on host machine with name "file1.txt"
Now, copy inside container c1
$ docker cp file1.txt c1:\file1.txt

WHERE 
    docker cp       Command to copy files between host and container        
                    Not supported on Docker Desktop (Windows mode)

NOTE: Incase of an ERROR stating name "C1" already used by another container,
      either use new name or delete old container.
      $ docker rm c1 
      To stop the container 
      $ docker stop c1