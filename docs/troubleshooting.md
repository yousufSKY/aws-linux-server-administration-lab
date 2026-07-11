# Troubleshooting Guide

This document outlines the common issues encountered while configuring and connecting to the Amazon Linux EC2 instance using SSH, along with the troubleshooting steps performed to resolve them.

---

# 1. SSH Connection Timed Out

## Problem

Unable to establish an SSH connection to the EC2 instance.

```
ssh: connect to host <Public-IP> port 22: Connection timed out
```

## Possible Causes

- Security Group does not allow SSH (TCP Port 22)
- Internet Gateway not attached
- Incorrect Route Table association
- EC2 instance is stopped
- Incorrect Public IPv4 Address

## Resolution

- Verified the EC2 instance was running.
- Confirmed Security Group allowed inbound SSH on TCP Port 22.
- Verified Internet Gateway attachment.
- Confirmed Public Route Table contained:

```
0.0.0.0/0 → Internet Gateway
```

- Rechecked the instance Public IPv4 Address.

---

# 2. Permission Denied (Public Key)

## Problem

```
Permission denied (publickey)
```

## Possible Causes

- Incorrect private key
- Wrong username
- Invalid file permissions on the PEM key

## Resolution

Ubuntu

```bash
chmod 400 aws-key.pem
```

Connected using

```bash
ssh -i aws-key.pem ec2-user@<Public-IP>
```

---

# 3. Host Key Verification Failed

## Problem

```
WARNING: REMOTE HOST IDENTIFICATION HAS CHANGED
```

## Resolution

Removed the previous host key from the known_hosts file and reconnected.

---

# 4. Unable to Ping External Hosts

## Problem

```
ping google.com
```

failed.

## Possible Causes

- No Internet Gateway
- Incorrect Route Table
- DNS resolution issue

## Resolution

Verified:

- Internet Gateway
- Route Table
- Public IP Assignment
- DNS Resolution

Successfully validated Internet connectivity.

---

# 5. Package Update Failed

## Problem

Unable to update packages.

## Resolution

Verified internet connectivity using:

```bash
ping google.com
```

Updated package repository:

```bash
sudo dnf check-update
sudo dnf update -y
```

---

# 6. SSH Client Not Installed (Windows)

## Problem

PowerShell could not recognize the SSH command.

## Resolution

Verified that the OpenSSH Client feature was installed on Windows 11.

---

# Best Practices Followed

- Restricted PEM key permissions.
- Used the default EC2 username.
- Allowed only required inbound ports.
- Verified connectivity before administration.
- Confirmed package updates completed successfully.

---

# Troubleshooting Workflow

1. Identify the issue.
2. Collect error messages.
3. Verify AWS networking configuration.
4. Validate Security Group rules.
5. Confirm SSH configuration.
6. Test connectivity.
7. Apply corrective action.
8. Verify successful resolution.
