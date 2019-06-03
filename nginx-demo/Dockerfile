# Filename MUST BE "Dockerfile"
# Base Image
FROM nginx:1.7.9

#Optional Labels (Added in META-DATA)
LABEL  Author="Mahendra Shinde"

#Commands tobe executed inside new container
copy index.html /usr/share/nginx/html

# To Trigger a BUILD, Run command:
#  docker build -t myapp:v2 . 