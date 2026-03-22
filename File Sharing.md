#computing 

# File Sharing

## Installing Samba

```shell
sudo apt update
sudo apt install samba
sudo ufw allow samba
```

## Making the Folder

```shell
sudo mkdir /share
sudo chmod 777 /share
```

## Adding the Folder to Samba

```shell
sudo nvim /etc/samba/smb.conf
```

Scroll to the bottom and add:
```txt
[share]
path = /share
browseable = yes
read only = no
guest ok = no
```

## Add Password to Samba

```shell
sudo smbpasswd -a digi
sudo systemctl enable smbd
sudo systemctl enable nmbd
sudo systemctl restart smbd
sudo systemctl restart nmbd
```

## Connect to Samba 

```shell
sudo mount -t cifs -o username=digi //192.168.122.8/share /mnt/samba
```
