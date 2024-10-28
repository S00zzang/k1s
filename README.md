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
```

# 0.2/tree
```
# Connect nginx run -> blog run
# Add blog 2, 3, 4
```

``` bash
# run

sudo docker build -t blog docker/httpd
sudo docker run -d --name blog-1 --rm blog
sudo docker run -d --name blog-2 --rm blog
sudo docker run -d --name blog-3 --rm blog
sudo docker run -d --name blog-4 --rm blog
sudo docker build -t lb docker/nginx
sudo docker run -d --name ngix_lb -p 8949:80 --link blog-1 --link blog-2 --link blog-3 --link blog-4 --rm lb
```

