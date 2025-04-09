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

[MobaExtreme](https://mobaxterm.mobatek.net/download.html) is a handy tool to help.

Copy or Move **libsmartunified.so** file  to  **/var/local/virl2/.local/lib/smart/**  using console.
To get root access type:
```
sudo -E -s
mv /tmp/libsmartunified.so /var/local/virl2/.local/lib/smart/
```
>
>Now Reboot the CML VM.

Now login with Web UI into CML and go to **Tools > System Administration > Licensing** and search **UDI**.

Now copy the **SN: XXXXXXXXXXX and UUID: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX**

![License UDI](Tools-Sysadmin-License.PNG "License UDI")

![License UDI](Tools-Sysadmin-License-UDI.PNG "License UDI")


Download and open **license.txt** file with notepad and paste the

SN: and UUID to under **S: XXXXXXXXXXX,U:XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX** and save the **license.txt** file.





