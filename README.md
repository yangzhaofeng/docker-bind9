# docker-bind9

  
# Start bind9 container with local dictionary

It contains all the configs and will be mounted under /etc/bind/

    docker run -itd \
	--restart=always \
	--name=bind9 \
	--net=host \
	--privileged \
	-v /srv/docker/bind:/etc/bind \
	yangzhaofengsteven/bind9 -g

