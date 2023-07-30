# rpi image configuration

## 0. Requirements

Install ansible on your computer:
```bash
pip3 install ansible
```

## 1. Create the shared ssh key
```bash
ssh-keygen -f rpi-key
```

## 2. Raspberry Pi Imager

1. Select `Ubuntu Server 22.04.2 LTS (64 bits)` as the Operating System
2. Seclet the SD card as the Storage
3. Open Settings
   1. Set the hostname `rpi-<number>`
   2. Paste your ssh public key
   3. Add username & password
4. Write

After that, you should be able to connect to the raspberrt pi with this commant:
```bash
ssh <username>@<ip-addr> -i rpi-key
```

## 3. Ready to run playbooks

```bash
cd ansible
ansible-playbook configure.yml
```


