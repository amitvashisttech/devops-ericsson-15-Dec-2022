## Deploy First Nginx Pod & Expose the same to LoadBalancer

```
 520  kubectl  get nodes 
  521  kubectl run hello-nginx --image=nginx --port=80 
  522  kubectl  get pods 
  523  kubectl  describe pods hello-nginx
  524  kubectl  get pods 
  525  kubectl  get pods -o wide 
  526  kubectl get svc 
  527  kubectl get pods 
  528  kubectl  expose pod hello-nginx --type=LoadBalancer
  529  kubectl get pods 
  530  kubectl get svc 
  531  kubectl  delete svc hello-nginx
  532  kubectl get pods 
  533  kubectl delete pod hello-nginx

```
