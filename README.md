# GPG and SSH

This repository is for those who want their commits to be verified.

You can configure it easily if you follow the following steps...

## Basic Git Configuration

```bash
git config --global user.name "Your Name"
```

```bash
git config --global user.email name@mail.com
```

```bash
git config --global core.editor "code --wait"
```

```bash
git config --global core.autocrlf input
```

## Configure SSH
### Generate SSH

```bash
ssh-keygen -t rsa -b 4096 -C "name@correo.com"
```
### Get Code
```bash
cat ~/.ssh/id_rsa.pub
```

### Go configure github by copying the code

### Test connection
```bash
ssh -T git@github.com
```

## Configure GPG

### Generate GPG Key
```bash
gpg --full-generate-key
```

### Get ID

```bash
gpg --list-secret-keys --keyid-format=long
```

Copy the code that is after the slash in the sec section

Example

3AA5C34371567BD2

### Get Key for github

```bash
gpg --armor --export 3AA5C34371567BD2
```

### Configure key on github


## Tell git to sign your commits with gpg

### Git use gpg
```bash
git config --global --unset gpg.format
```

### get gpg ID
```bash
gpg --list-secret-keys --keyid-format=long

```

### Set key for git

```bash
git config --global user.signingkey 3AA5C34371567BD2

```

### Sign commits with gpg
```bash
git config --global commit.gpgsign true
```
