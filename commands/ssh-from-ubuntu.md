# Ubuntu SSH Commands

This document contains the commands used to establish a secure SSH connection from an Ubuntu workstation to an Amazon Linux EC2 instance and perform basic Linux administration tasks.

---

## 1. Navigate to the Directory Containing the PEM Key

```bash
cd ~/Downloads
```

---

## 2. Change File Permissions

```bash
chmod 400 aws-key.pem
```

This restricts access to the private key and is required before SSH authentication.

---

## 3. Connect to the EC2 Instance

```bash
ssh -i aws-key.pem ec2-user@<EC2-Public-IP>
```

---

## 4. Verify User Information

```bash
whoami
id
groups
```

---

## 5. Verify System Information

```bash
hostname
uname -a
cat /etc/os-release
uptime
date
```

---

## 6. File System Navigation

```bash
pwd
ls
ls -l
cd /home/ec2-user
```

---

## 7. Network Verification

```bash
hostname -I
ip addr
ip route
ping google.com
```

---

## 8. Disk and Memory Information

```bash
df -h
lsblk
free -h
```

---

## 9. Process Monitoring

```bash
top
ps -ef
```

---

## 10. Package Management

Amazon Linux 2023

```bash
sudo dnf check-update
sudo dnf update -y
```

---

## 11. Service Management

```bash
systemctl status sshd
systemctl list-units --type=service --state=running
```

---

## 12. File Operations

```bash
mkdir project
touch test.txt
cp test.txt project/
mv test.txt sample.txt
rm sample.txt
```

---

## 13. Logout

```bash
exit
```

---

