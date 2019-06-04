## TWO TIER App : ASP.NET With MS-SQL Database 

1. From Your Docker Host (Azure VM), download the sample application using URL:
    `https://github.com/mahendra-shinde/mssql-aspnet-docker-demo-app/archive/master.zip`

    The exact command is (Single line):

    ```
    $ invoke-webrequest 
        -url https://github.com/mahendra-shinde/mssql-aspnet-docker-demo-app/archive/master.zip 
        -UseBasicParsing
        -OutFile demo1.zip
    ```

    Then extract the contents into new directory
    
    ```
    $ mkdir c:\demoapp
    $ Expand-Archive demo1.zip c:\demoapp
    $ cd \demoapp
    ```

2.  Open webapps subfolder and view Dockerfile
  
    ```
    $ cd mssql-aspnet-docker-demo-app-master\webapp
    $ notepad Dockerfile
    ```

3.  Review docker-compose file from same directory
    
    ```
    $ notepad docker-compose.yml
    ```

4.  Start Building and Deploying application using command:
  
    ```
    $ docker-compose up 
    ```


