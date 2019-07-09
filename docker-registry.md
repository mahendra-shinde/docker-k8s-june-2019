## Create Image repository on docker-hub and Push image

1. Login in hub.docker.com with your docker id
2. Click "Create Repository" button
3. enter name for repository and select "public"
4. Click "Create" button
5. Switch to docker cli
6. Login with docker cli (Persistent login)
    
    $ docker login 
    
    Enter username: <Username>
    Enter password: <password>
7. Pull my custom image
    
        $ docker pull mahendrshinde/myapp2:2
8. Rename image with your account name
    
        $ docker tag mahendrshinde/myapp2:2 {youraccount}/myapp2:2
    
    WHERE:
        replace {youraccount} with docker account you have created!
        please remove curly braces as well
9.  Use docker push to start upload
    
        $ docker push {youraccount}/myapp2:2

