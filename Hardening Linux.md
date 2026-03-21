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
- 