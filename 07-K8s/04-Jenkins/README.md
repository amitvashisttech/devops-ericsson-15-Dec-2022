```
510  mkdir 04-Jenkins
  511  ls
  512  cd 04-Jenkins/
  513  s
  514  ls
  515  ls
  516  cd 02-Jenkins/
  517  ls
  518  cat sa.yaml 
  519  kubectl  create ns jenkins-demo --dry-run -o yaml 
  520  kubectl  create ns jenkins-demo --dry-run -o yaml > 01-NameSpace.yaml
  521  ls
  522  cat 01-NameSpace.yaml 
  523  kubectl  create sa jenkins-admin -n jenkins-demo --dry-run -o yaml > 02-ServiceAccount.yaml
  524  cat 02-ServiceAccount.yaml 
  525  vim 03-Role-and-Binding.yaml
  526  ls
  527  kubectl  apply -f 01-NameSpace.yaml 
  528  kubectl  get ns 
  529  kubectl  apply -f 02-ServiceAccount.yaml 
  530  kubectl  get sa -n jenkins-demo
  531  kubectl  apply -f 03-Role-and-Binding.yaml 
  532  kubectl  get roles -n jenkins-demo
  533  kubectl  get rolebinding  -n jenkins-demo
  534  ls
  535  ls
  536  vim deploy.yaml 
  537  cat deploy.yaml 
  538  vim 04-PVC.yaml
  539  kubectl  api-resources 
  540  kubectl  api-resources  | grep -i pvc 
  541  vim 04-PVC.yaml
  542  kubectl  apply -f 04-PVC.yaml 
  543  kubectl  get pvc -n jenkins-demo
  544  vim 05-Deployment.yaml 
  545  ls
  546  kubectl  apply -f 05-Deployment.yaml 
  547  kubectl get pods -n jenkins-demo 
  548  watch -n .5 kubectl get pods -n jenkins-demo 
  549  ls
  550  vim 06-Service.yaml 
  551  kubectl  apply -f 06-Service.yaml 
  552  watch -n .5 kubectl get pods -n jenkins-demo 
  553  kubectl get pods -n jenkins-demo 
  554  kubectl get svc  -n jenkins-demo 
  555  kubectl get pods -n jenkins-demo 
  556  kubectl logs -f jenkins-deployment-9c84d699-tfhkb -n jenkins-demo 
```
