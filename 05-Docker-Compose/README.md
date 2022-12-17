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



T-Shooting  - of Jenkins & Docker

```
 401  cd 03-App-Code/
  402  ls
  403  cd mywebapp/
  404  ls
  405  cp -rf ../../05-Docker-Compose/04-MyWebApp/Dockerfile .
  406  cp -rf ../../05-Docker-Compose/04-MyWebApp/docker-compose.yaml .
  407  ls
  408  cd ..
  409  ls
  410  cd ..
  411  ls
  412  git add . ; git commit -m "04-Docker" ; git push
  413  ls
  414  git add . ; git commit -m "04-Docker" ; git push
  415  git branch
  416  git checkout pipeline
  417  ls
  418  git branch
  419  ls
  420  cp -rf 02-Pipeline-Archive 03-Pipeline-Docker-Compose
  421  ls
  422  vim 03-Pipeline-Docker-Compose
  423  ls
  424  cp -rf 03-Pipeline-Docker-Compose Jenkinsfile
  425  ls
  426  git add . ; git commit -m "Var Pipeline" ; git push
  427  cat /etc/passwd
  428  cat /etc/passwd| grep -i jenkins
  429*
  430  vim Jenkinsfile
  431  git add . ; git commit -m "Var Pipeline with Sudo" ; git push
  432  sudo usermod -aG docker jenkins
  433  ls
  434  vim Jenkinsfile
  435  git add . ; git commit -m "Var Pipeline without Sudo" ; git push
  436  sudo su - jenkins
  437  ls
  438  which docker-compose
  439  chmod +x /usr/local/bin/docker-compose
  440  sudo chmod +x /usr/local/bin/docker-compose
  441  ls
  442  systemctl restart jenkins
  443  sudo systemctl restart jenkins
  444  sudo systemctl restart docker
  445  which docker-compose
  446  ls -ltr docker-compose
  447  sudo ls -ltr /usr/local/bin/docker-compose
  448  sudo chmod 777 /usr/local/bin/docker-compose
  449  sudo ls -ltr /usr/local/bin/docker-compose
  450  docker ps
  451  docker kill 9726610682a9
```
