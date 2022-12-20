```
  523  cd 02-Deployments/
  524  ls
  525  kubectl get pods
  526  kubectl  delete pod hello-k8s-2
  527  ls
  528  kubectl  apply -f 01-helloworld.yaml
  529  kubectl  get deploy
  530  kubectl  get pods
  531  kubectl  expose deploy helloworld-deployment --type=LoadBalancer
  532  kubectl  get svc
  533  ls
  534  kubectl  get deploy
  535  kubectl  get deploy,rs
  536  kubectl  get deploy,rs,pods
  537  kubectl  describe deploy helloworld-deployment
  538  kubectl  scale --replicas=5 deploy -f 01-helloworld.yaml
  539  kubectl  scale --replicas=5  -f 01-helloworld.yaml
  540  cd
  541  kubectl set image deploy helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web:2
  542  kubectl  describe deploy helloworld-deployment
  543  kubectl set image deploy helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web:3
  544  kubectl set image deploy helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web:4
  545  kubectl  get deploy
  546  kubectl  get rs
  547  kubectl  rollout status deploy helloworld-deployment
  548  kubectl  rollout history deploy helloworld-deployment
  549  kubectl  rollout history deploy helloworld-deployment --revision=4
  550  kubectl  rollout history deploy helloworld-deployment --revision=3
  551  kubectl  rollout history deploy helloworld-deployment --revision=2
  552  kubectl  rollout history deploy helloworld-deployment --revision=1
  553  kubectl  rollout history deploy helloworld-deployment
  554  kubectl  rollout undo  deploy helloworld-deployment
  555  kubectl  rollout history deploy helloworld-deployment
  556  kubectl  rollout undo  deploy helloworld-deployment
  557  kubectl  rollout history deploy helloworld-deployment
  558  kubectl  rollout undo  deploy helloworld-deployment --to-revision=1
  559  kubectl  rollout history deploy helloworld-deployment
  560  kubectl  rollout history deploy helloworld-deployment --revision=7
  561  kubectl set image deploy helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web:4 --record
  562  kubectl  rollout history deploy helloworld-deployment
  563  kubectl set image deploy helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web:3 --record
  564  kubectl set image deploy helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web:2 --record
  565  kubectl set image deploy helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web --record
  566  kubectl  rollout history deploy helloworld-deployment
```
