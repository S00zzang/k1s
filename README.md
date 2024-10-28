# K1S
- https://hub.docker.com/_/httpd

# BUILD & RUN
```

# build
sudo docker build -t my-apache2 .

# run
sudo docker run -dit --name my-running-app -p 8949:80 my-apache2

# container
sudo docker exec -it my-running-app bash
