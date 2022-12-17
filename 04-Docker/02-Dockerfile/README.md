```
126  mkdir 02-Dockerfile/apache/v1 -p
  127  cd 02-Dockerfile/apache/v1/
  128  ls
  129  vim Dockerfile
  130  ls
  131  docker build -t myapache:v1 .
  132  ls
  133  docker images
  134  docker run -d myapache:v1
  135  docker ps
  136  docker inspect 50de435e7376
  137  curl 172.17.0.2
  138  ls
  139  cd ..
  140  ls
  141  curl 172.17.0.2
  142  ls
  143  docker ps
  144  curl -v 172.17.0.2
  145  ls
  146  cd ..
  147  ls
  148  cd apache/
  149  ls
  150  cp -rf v1 v2
  151  ls
  152  cd v2/
  153  ls
  154  vim Dockerfile
  155  ls
  156  docker build -t myapache:v2 .
  157  docker images
  158  docker run -d myapache:v2
  159  docker ps
  160  curl -v 172.17.0.3:80
  161  ls
  162  curl -v 172.17.0.3:80
  163  ls
  164  cd ..
  165  ls
  166  docker run -d -p 80:80  myapache:v2
  167  docker ps
  168  netstat -tulnp
  169  systemctl status docker
  170  ls
  171  docker ps
  172  docker kill 024beb6d8028
  173  docker ps
  174  ls
  175  cp -rf v2 v3
  176  ls
  177  cd v3/
  178  ls
  179  vim index.html
  180  ls
  181  vim Dockerfile
  182  docker build -t myapache:v3 .
  183  docker run -d -p 80:80  myapache:v3
  184  docker ps
```
