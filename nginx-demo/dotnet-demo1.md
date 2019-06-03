## Building DOTNET Core container image

1. Create a folder "dotnet-demos" in your C drive
2. Open Command prompt / Powershell in c:\dotnet-demos
3. Run following command to create new MVC Application

    $ dotnet new mvc -n myapp1

4.  Test run the project

    $ cd myapp1
    $ dotnet run 

5.  Test application using URL:
    > http://localhost:5000/

6.  Publish Application

    $ mkdir publish
    $ dotnet publish -o publish

7.  Create a Dockerfile in Application root folder

    ```
    FROM microsoft/dotnet:2-aspnetcore-runtime
    WORKDIR /app
    COPY publish/* /app/
    CMD dotnet run 
    
    ```

