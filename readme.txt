# this image is for centos 7

git clone https://github.com/kmamtora/docker-httpd.git

#To build the image run
docker build -t centhttpd:v1.0 .

#To run the container
docker run -d --name web -p 8080:80 centhttpd:v1.0

#Run the Apache container with source code volume mapped to it
docker run -d --name myweb -p 8081:80 -v /root/custom/www/:/var/www/html/ centhttpd:v1.0
