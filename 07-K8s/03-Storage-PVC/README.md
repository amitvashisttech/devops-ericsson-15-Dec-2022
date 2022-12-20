544  mkdir 03-Storage-PVC
  545  ls
  546  cd 03-Storage-PVC/
  547  ls
  548  mv ../../../storageclass.yaml . 
  549  ls
  550  mv storageclass.yaml 01-StorageClass.yaml 
  551  ls
  552  cat 01-StorageClass.yaml 
  553  kubectl  apply -f 01-StorageClass.yaml 
  554  kubectl  get sc 
  555  ls
  556  mv ../../../pvc.yaml . 
  557  ls
  558  mv pvc.yaml 02-Pvc.yaml
  559  ls
  560  vim 02-Pvc.yaml 
  561  kubectl  apply -f 02-Pvc.yaml 
  562  kubectl  get pvc 
  563  ls
  564  cd ..
  565  ls
  566  cd 03-Storage-PVC/
  567  ls
  568  cp -rf ../18-Volume-NFS/03-nfs-busybox-rc.yaml . 
  569  cp -rf ../18-Volume-NFS/04-web-rc-pvc.yaml 
  570  cp -rf ../18-Volume-NFS/04-web-rc-pvc.yaml .
  571  cp -rf ../18-Volume-NFS/05-nfs-web-svc.yaml . 
  572  ls
  573  kubectl  get pvc 
  574  ls
  575  vim 03-nfs-busybox-rc.yaml 
  576  ls
  577  kubectl  apply -f 03-nfs-busybox-rc.yaml 
  578  vim 04-web-rc-pvc.yaml 
  579  ls
  580  kubectl  get pvc 
  581  ls
  582  kubectl get pods 
  583  ls
  584  kubectl  apply -f 04-web-rc-pvc.yaml 
  585  vim 05-nfs-web-svc.yaml 
  586  ls
  587  kubectl  apply -f 05-nfs-web-svc.yaml 
  588  vim 03-nfs-busybox-rc.yaml 
  589  ls
  590  cat 04-web-rc-pvc.yaml 
  591  ls
  592  cat 05-nfs-web-svc.yaml 
  593  kubectl  get svc 
  594  kubectl  get pods 
  595  kubectl  exec -it  nfs-busybox-9jksx -- sh 
  596  ls
  597  kubectl delete -f 03-nfs-busybox-rc.yaml 
  598  kubectl  get pvc 
  599  vim 03-nfs-busybox-rc.yaml 
  600  kubectl  apply -f 03-nfs-busybox-rc.yaml 
  601  kubectl  get pvc 
  602  ls
  603  cd ..
  604  ls
  605  rm -rf 18-Volume-NFS/
  606  kubectl  delete -f 03-Storage-PVC/
  607  kubectl  get pods 
  608  s
  609  ls
  610  cd ..
  611  ls
  612  git add . ; git commit -m "03-Storage" ; git push 
  613  cd
  614  ls
  615  cd devops-ericsson-15-Dec-2022/
  616  ls
  617  cd 07-K8s/03-Storage-PVC/
