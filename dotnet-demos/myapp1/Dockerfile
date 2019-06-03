FROM microsoft/dotnet:2-aspnetcore-runtime

WORKDIR /app

COPY publish/* /app/

## Define an Entrypoint for new container
CMD dotnet myapp1.dll

# docker build -t myapp:v3 . 
# docker run --name c2 -d -p 5000:80 myapp:v3