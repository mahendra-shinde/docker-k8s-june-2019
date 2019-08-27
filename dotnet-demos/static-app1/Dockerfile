## Import BASE IMAGE
FROM mcr.microsoft.com/windows/servercore/iis:windowsservercore-ltsc2016

## SWITCH WORKING DIRECTORY
WORKDIR /inetpub/wwwroot

## DELETE SOME FILES
RUN del iisstart.htm

## COPY NEW FILES FROM CURRENT DIRECTORY INTO WORKING DIRECTORY
COPY *.htm ./


## To Build Container Image, use command:
## The "DOT" at the end of following command represents directory
## which contains all three files (htm and Dockerfile)
# $ docker build -t myapp:2 .  

## To Test Run container from new image
# $ docker run --name c4 -d myapp:2
## To Get IP Address of container 
# $ docker inspect c4
## Open web browser to visit container's IP address



