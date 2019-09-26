Network demo

# Create new Network
$ docker network create -d transparent net1 --subnet 172.17.0.0/16

# Create a new container inside network net1
$ docker run --name c1 --hostname c1 -d --net net1 \
    mcr.microsoft.com/windows/servercore/iis

# Create second container inside network net1
$ docker run --name c2 --hostname c2 -d --net net1 \
    mcr.microsoft.com/windows/servercore/iis

# Create third container NOT in net1
$ docker run --name c3 --hostname c3 -d \
     mcr.microsoft.com/windows/servercore/iis
    
# Enter INSIDE the container c1
$ docker exec -it c1 cmd
$ ping c2 
## Should be successful
$ ping c3
## Should FAIL!
$ exit

## Stop all containers and remove them
$ docker stop c1 c2 c3
$ docker rm c1 c2 c3