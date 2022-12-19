```
 906  ls
  907  mkdir 01-Inventory
  908  ls
  909  cd 01-Inventory/
  910  ls
  911  vim hosts
  912  ip addr
  913  vim hosts
  914  ls
  915  ansible all -i hosts -m ping -u azureuser -k
  916  ssh azureuser@10.0.0.4
  917  ls ~/.ssh/known_hosts
  918  cat  ~/.ssh/known_hosts
  919  ansible all -i hosts -m ping -u azureuser -k
  920  df -h
  921  ansible all -i hosts -m command -d 'df -hTP' -u azureuser -k
  922  ansible all -i hosts -m command -a 'df -hTP' -u azureuser -k
  923  ls
  924  vim hosts
  925  ansible all -i hosts -m command -a 'df -hTP' -u azureuser -k
  926  ssh azureuser@10.0.0.5
  927  ssh azureuser@10.0.0.6
  928  ls
  929  ansible all -i hosts -m command -a 'df -hTP' -u azureuser -k
  930  ansible all -i hosts -m command -a 'uname -a' -u azureuser -k
  931  ansible 10.0.0.5 -i hosts -m command -a 'uname -a' -u azureuser -k
  932  ansible 10.0.0.7 -i hosts -m command -a 'uname -a' -u azureuser -k
  933  vim hosts
  934  ansible ansible -i hosts -m command -a 'uname -a' -u azureuser -k
  935  ansible web -i hosts -m command -a 'uname -a' -u azureuser -k
  936  vim hosts
  937  ls
  938  ansible web -i hosts -m command -a 'uname -a'
  939  ansible web -i hosts -m command -a 'df -h'
  940  ansible ansible -i hosts -m command -a 'df -h'
  941  vim
  942  vim hosts
  943  ansible dc -i hosts -m command -a 'df -h'
```


## Demo 2 & 3 

```
 986  cd ../02-Ansible-Config/
  987  ls
  988  vim ansible.cfg
  989  ls
  990  ansible dc -m command -a 'df -h'
  991  vim ansible.cfg
  992  ansible dc -m command -a 'df -h'
  993  ls
  994  cd ..
  995  ls
  996  cp -rf 02-Ansible-Config 03-Playbook
  997  ls
  998  cd 03-Playbook/
  999  ls
 1000  vim webserver.yaml
 1001  ls
 1002  ansible-playbook webserver.yaml
 1003  curl 10.0.0.6
 1004  curl 10.0.0.5
 1005  ls
 1006  vim webserver.yaml
 1007  ansible-playbook webserver.yaml
 1008  vim webserver.yaml
 1009  ansible-playbook webserver.yaml
```
