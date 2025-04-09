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




