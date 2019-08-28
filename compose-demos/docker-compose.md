## docker-compose : Managing multi-container application

1. docker-compose.yaml or docker-compose.yml
    Define "Services", "Volumes", "Networks"

2. docker-compose.exe Command line utility for processing 'docker-compose.yaml' file.
    config      : Validate the YAML file
    create      : Validate the YAML file and create all services, networks & volumes.
    start       : Start the containers defined by service. (services Must exists!)
    stop        : Stop all containers defines by service.
    up          : Combination of 'create' and 'start'
    rm          : Remove everything
    down        : Combination of 'stop' and 'rm'

## Demo Steps

1.  Download the docker-compose.yml file into a new directory 'demo1'

2.  Open powershell or cmd in 'demo1' directory and try following command to validate the YAML file.

    ```shell
    $ docker-compose config
    ```

    NOTE:   Either you would get ERROR or you would get the contents of YAML file (without comments).

3.  In case of NO-ERROR, just try to create and start all services.
    The "-d" would launch in DETACHED mode

    ```shell
    $ docker-compose up -d
    $ docker-compose ps
    ```

4.  Try accessing application from web address `http://localhost:8080`