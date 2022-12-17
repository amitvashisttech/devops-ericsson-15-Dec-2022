```

486  mkdir 05-Docker-Compose
  487  ls
  488  cd 05-Docker-Compose/
  489  ls
  490  mkdir 00-Setup
  491  ls
  492  vim 00-Setup/install-docker-compose.sh
  493  cd 00-Setup/
  494  ls
  495  chmod +x install-docker-compose.sh
  496  ./install-docker-compose.sh
  497  sudo ./install-docker-compose.sh
  498  docker-compose version
  499  ls
  500  cd ..
  501  ls
  502  mkdir 01-Nginx
  503  ls
  504  cd 01-Nginx/
  505  ls
  506  vim docker-compose.yaml
  507  ls
  508  docker-compose up -d
  509  docker-compose ps
  510  docker ps
  511  curl localhost:8090
  512  ls
  513  docker-compose kill
  514  docker-compose rm
  515  ls
  516  cd ..
  517  ls
  518  cp -rf 01-Nginx 02-MyApache
  519  ls
  520  cd 02-MyApache/
  521  ls
  522  docker images
  523  vim docker-compose.yaml
  524  ls
  525  docker-compose up -d
  526  docker-compose ps
  527  docker ps
  528  ls
  529  docker-compose kill
  530  docker-compose rm
  531  ls
  532  cd ..
  533  ls
  534  cp -rf 02-MyApache 03-ImageBuild
  535  ls
  536  cp -rf ../04-Docker/02-Dockerfile/apache/v3/* 03-ImageBuild/
  537  ls
  538  cd 03-ImageBuild/
  539  ls
  540  cat Dockerfile
  541  ls
  542  vim index.html
  543  ls
  544  > docker-compose.yaml
  545  ls
  546  vim docker-compose.yaml
  547  ls
  548  docker-compose up -d
  549  docker-compose ps
  550  curl localhost:30080
  551  ls
  552  vim index.html
  553  docker-compose up -d
  554  docker-compose up -d --build
  555  docker-compose ps
  556  curl localhost:30080
  557  vim index.html
  558  docker-compose up -d --build
  559  curl localhost:30080
  560  ls

```
