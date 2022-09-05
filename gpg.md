# GPG

### Setup

Generate new key:
```bash
gpg --expert --full-gen-key
```
> Elliptic curve keys are not supported.

List your keys:
```bash
gpg --list-keys
```

Export private key:
```bash
gpg --export-secret-keys 74F6A05787B8EB830A61994A7872F37A0D8C34F6 | base64 > private.key
```

Import key:
```bash
cat private.key | base64 -d | gpg --import -
```

Delete keys:
```bash
gpg --delete-secret-keys 74F6A05787B8EB830A61994A7872F37A0D8C34F6
gpg --delete-keys 74F6A05787B8EB830A61994A7872F37A0D8C34F6
```

---

### keyserver

Get your Public Key
```bash
gpg --armor --export shubhamtatvamasi@gmail.com
```

Upload it to: https://keyserver.ubuntu.com

---

### Install

Install Gnu GPG tool:
```bash
brew install gnupg
```
> command is for macOS
