## Import BASE IMAGE
FROM mcr.microsoft.com/windows/servercore/iis:windowsservercore-ltsc2016

## SWITCH WORKING DIRECTORY
WORKDIR /inetpub/wwwroot

## DELET SOME FILES
RUN del iisstart.htm

## COPY NEW FILES
COPY *.htm ./


## To Build Container Image, use command:
# $ docker build -t myapp:2 .  

## To Test Run container from new image
# $ docker run --name c4 -d myapp:2



