# docker-bind9


# Build a data container
    docker run --name bind9-data -v /disk/ssd/configs/bind9:/etc/bind busybox true

  
# Start bind9 container with the data container

It contains all the configs and will be mounted under /etc/bind/

    docker run -d -t --name bind9 -p 953:953 -p 53:53 -p 53:53/udp --dns=127.0.0.1 --dns-search=factual.com --volumes-from bind9-data factual/bind9
