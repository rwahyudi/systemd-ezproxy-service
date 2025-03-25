# EZProxy service file for systemd start/stop
## ezproxy.service

EZProxy installed in /usr/local/ezproxy/ directory and run as ezproxy user.
```shell
useradd -d /usr/local/ezproxy/ ezproxy
su - ezproxy 
wget 'https://help.oclc.org/@api/deki/files/9850/' -O ezproxy.7.3.bin
ln -s ezproxy -> ezproxy.7.3.bin
```
OS : RHEL9

### Installation:

1. Download file : 

```Ruby
wget "https://github.com/rwahyudi/systemd-ezproxy-service/raw/refs/heads/master/ezproxy.service" -O /usr/local/ezproxy/ezproxy.service
```

2. Create Symlink :

```Shell
ln -s /usr/local/ezproxy/ezproxy.service /lib/systemd/system/ezproxy.service 
```
3. Reload systemd, start and enable ezproxy service:
  ```
systemctl daemon-reload 
systemctl enable ezproxy.service --now
```




