# study
***
***
### Repository created to take a note of settings used in system and Nework Administration practices
***
### Cisco CML Setup After Installation

#### Instruction
Right after CML VM installation SSH port to be changed into 1122 in CLI in order to setup license porblem.
>
>If SSH server is not installed
```
apt update
apt install openssh-server
systemctl enable ssh
```
>
>change SSH port
```
nano /etc/ssh/sshd_config
```
![SSH Server port change](sshd_config_Port.PNG "SSH server Port change")

>
>restart SSH Server
```
systemctl restart ssh
systemctl status ssh
```

SSH to CML VM via your host machine and copy **libsmartunified.so** into **/tmp**
[MobaExtreme]([https://link-url-here.org](https://mobaxterm.mobatek.net/download.html) is a handy tool to help.




