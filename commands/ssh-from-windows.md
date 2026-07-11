# Windows Powershell SSH Commands

This document contains the PowerShell commands used to establish a secure SSH connection from a Windows 11 workstation to an Amazon Linux EC2 instance.

---

## 1. Navigate to the Directory Containing the PEM Key

```powershell
cd Downloads
```

---

## 2. Connect to the EC2 Instance

```powershell
ssh -i aws-key.pem ec2-user@<EC2-Public-IP>
```

---

## 3. Verify User Information

```bash
whoami
id
groups
```

---

## 4. Verify System Information

```bash
hostname
uname -a
cat /etc/os-release
uptime
date
```

---

## 5. File System Navigation

```bash
pwd
ls
ls -l
cd /home/ec2-user
```

---

## 6. Network Verification

```bash
hostname -I
ip addr
ip route
ping google.com
```

---

## 7. Disk and Memory Information

```bash
df -h
lsblk
free -h
```

---

## 8. Process Monitoring

```bash
top
ps -ef
```

---

## 9. Package Management

Amazon Linux 2023

```bash
sudo dnf check-update
sudo dnf update -y
```

---

## 10. Service Management

```bash
systemctl status sshd
systemctl list-units --type=service --state=running
```

---

## 11. File Operations

```bash
mkdir project
touch test.txt
cp test.txt project/
mv test.txt sample.txt
rm sample.txt
```

---

## 12. Logout

```bash
exit
```

---

