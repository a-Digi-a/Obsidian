# Hardening Linux

## Installing sudo and adding the user to the sudo group

```shell
su -
apt update
apt install sudo
usermod -aG sudo digi
# ctrl + d
```

## SSH config

```shell
sudo apt install neovim
sudo nvim /etc/ssh/sshd_config
```

### What to edit

- Change port to some random high number (47398)
- PasswordAuthentication no
- KbdInteractiveAuthentication no
- PermitRootLogin no

After edits:
```shell
sudo systemctl restart --now sshd
```

Then test in a different terminal if ssh is working **but keep your first one open!**

## UFW firewall

```shell
sudo apt install ufw
sudo ufw allow 47398 # allow the port you set earlier
sudo ufw deny 22 # disable default ssh port
sudo ufw enable
```

## Fail2ban

Fail2ban blocks suspicious ip's

```shell
sudo apt install fail2ban
sudo systemctl enable --now fail2ban
sudo fail2ban-client status
```