# We need to setup a new virtual machine for our Jenkins Demo. 

## Create a resource group
```
az group create --name jenkins-rg --location eastus
```

## Create a virtual machine
```
az vm create --resource-group jenkins-rg  --name jenkinsVM --image "UbuntuLTS"  --admin-username azureuser    --admin-password Pass@word1234! --size="Standard_D2s_v3"
```

## Open port 80 for web traffic
```
az vm open-port --port 80 --resource-group jenkins-rg --name jenkinsVM
```




# Deploying Jenkins


### Let's login to newly create Jenkins Azure VM
```
ssh <username>@<public-ip>
```

### First, add the repository key to the system:
```
wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo apt-key add -
```

### Debian package repository address to the server’s sources.list:
```
sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
```

### When both of these are in place, run update so that apt will use the new repository:
```
sudo apt update
```

### Finally, install Jenkins and its dependencies:
```
sudo apt install default-jdk jenkins -y 
```

## Starting Jenkins

### Let’s start Jenkins using systemctl:
```
sudo systemctl start jenkins
```

### Let’s check Jenkins status using systemctl:
```
sudo systemctl status jenkins
```


### Get your Public IP
```
curl ifconfig.me 
```

### Now try to open Jenkins in your Browser. 
```
http://your_server_ip_or_domain:8080
```


Note: In case you are getting error, then please do consider NSG & Open the required traffice flow for Jenkins with following commands as an example: 

### Run the following command form CLOUD SHELL: 
```
az vm open-port --port 8080 --resource-group jenkins-rg --name jenkinsVM --priority 101
```


### We should see the Unlock Jenkins screen, which displays the location of the initial password:
```
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```

### We’ll click the Install suggested plugins option, which will immediately begin the installation process:

### Setup your login by adding any user of your choice: 





