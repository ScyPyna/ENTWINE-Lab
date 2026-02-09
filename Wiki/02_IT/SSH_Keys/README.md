# Access to the Workstation via SSH (Step-by-Step Guide)

This workstation can be accessed **only via SSH using public/private keys**.

Each user must generate **their own SSH key** on their personal computer and send the **public key** to the system administrator.

---

## Before You Start

You must know:
- Your **username** on the workstation (example: `alice`)
- The **hostname** of the workstation (example: `workstation`)

In the examples below:
- `USERNAME` → your workstation username
- `WORKSTATION_HOSTNAME` → the workstation hostname

---

# macOS Instructions

## Step 1: Open the Terminal

1. Open **Terminal.app**
   - Finder → Applications → Utilities → Terminal
   - or search for “Terminal” using Spotlight

You should see a prompt similar to:

```text
alice@macbook ~ %
```

## Step 2: Generate an SSH key

In the terminal run: 

```text
ssh-keygen -t ed25519 -C "your.name@workstation" 
```

You will see: 

```text
Generating public/private ed25519 key pair.
Enter file in which to save the key (/Users/yourusername/.ssh/id_ed25519):

```
Press Enter to accept the default location.

You will then be asked to choose a passphrase:

```text
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
```

- The passphrase is optional but strongly recommended
- The passphrase will not be visible while typing

If the operation is successful, you will see output similar to:

```text
Your identification has been saved in /Users/yourusername/.ssh/id_ed25519
Your public key has been saved in /Users/yourusername/.ssh/id_ed25519.pub
The key fingerprint is:
SHA256:XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX your.name@workstation
```

Two files have now been created:
- `~/.ssh/id_ed25519` → private key (DO NOT SHARE)
- `~/.ssh/id_ed25519.pub` → public key

---

## Step 3: Display and send your public key

To display your public key, run:

```text
cat ~/.ssh/id_ed25519.pub
```
You will see a single long line starting with ssh-ed25519, for example:

```text
ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAI... your.name@workstation
```
Copy the entire line and send it to the workstation administrator.

## Step 4: Connect to the workstation

After the administrator confirms that your key has been installed, connect using:

```text
ssh USERNAME@WORKSTATION_HOSTNAME
```

Example:
```text
ssh alice@workstation
```
If this is your first connection, you will see:

```text
The authenticity of host 'workstation (XXX.XXX.XXX.XXX)' can't be established.
ED25519 key fingerprint is SHA256:YYYYYYYYYYYYYYYYYYYYYYYYYYYYYYY.
Are you sure you want to continue connecting (yes/no)?
```

Type:

```text
yes
```

If everything is correct, you will see a prompt like:

```text
alice@workstation:~$
```
# Windows Instructions

These instructions apply to Windows 10 and Windows 11 using the built-in OpenSSH client.

## Step 1: Open PowerShell

1. Click Start
2. Search for PowerShell
3. Open Windows PowerShell

You should see a prompt similar to:

```text
PS C:\Users\yourusername>
```

## Step 2: Generate an SSH key

Run: 

```text
ssh-keygen -t ed25519 -C "your.name@workstation"
```

You will see:

```text
Generating public/private ed25519 key pair.
Enter file in which to save the key (C:\Users\yourusername\.ssh\id_ed25519):
```

Press Enter to accept the default location.

You will be asked to choose a passphrase:

```text
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
```

- The passphrase is optional but recommended
- Nothing will be displayed while typing

If successful, you will see:

```text
Your identification has been saved in C:\Users\yourusername\.ssh\id_ed25519
Your public key has been saved in C:\Users\yourusername\.ssh\id_ed25519.pub
The key fingerprint is:
SHA256:XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX your.name@workstation
```

Two files have now been created:
- `id_ed25519` → private key (DO NOT SHARE)
- `id_ed25519.pub` → public key

---

## Step 3: Display and send your public key

To display your public key, run:

```text
type $env:USERPROFILE\.ssh\id_ed25519.pub
```

You will see a single line similar to:

```text
ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAI... your.name@workstation
```

Copy the entire line and send it to the workstation administrator.

---

## Step 4: Connect to the workstation

After your key has been installed:

```text
ssh USERNAME@WORKSTATION_HOSTNAME
```

Example:

```text
ssh alice@workstation
```

On first connection you may see:

```text
The authenticity of host 'workstation (XXX.XXX.XXX.XXX)' can't be established.
Are you sure you want to continue connecting (yes/no)?
```

Type:

```text
yes
```

A successful login looks like:

```text
alice@workstation:~$
```

---

## Optional: SSH Configuration File (Recommended)

To simplify future connections, you can create an SSH configuration file.

### Create the configuration file

File location:

```text
~/.ssh/config
```
Example content:

```text
Host workstation
    HostName WORKSTATION_HOSTNAME
    User USERNAME
    IdentityFile ~/.ssh/id_ed25519
```

After this, you can connect simply with:

```text
ssh workstation
```