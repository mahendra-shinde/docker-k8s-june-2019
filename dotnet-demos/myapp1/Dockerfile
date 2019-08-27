### dotnet build -o publish

FROM mcr.microsoft.com/dotnet/core/aspnet:2.2.2-nanoserver-sac2016

WORKDIR /app
## Ensure PUBLISH directory contains build artifacts (DLLs)
## if not, run `dotnet build -o publish`
COPY publish/* /app/

## Define an main process for new container
CMD dotnet myapp1.dll

# docker build -t myapp:v3 . 
# docker run --name c2 -d -p 5000:80 myapp:v3