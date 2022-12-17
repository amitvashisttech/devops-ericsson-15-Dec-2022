# Run Docker as a regular user

````
docker version 
echo ${USER}
```

```
sudo usermod -aG docker ${USER}
```

```
sudo systemctl restart docker 
```

```
exit
``` 
