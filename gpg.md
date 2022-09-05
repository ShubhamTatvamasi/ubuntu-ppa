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
gpg --export-secret-keys C12BA9B9AC50B47C2EC87B5A3767E58D5D276494 | base64 > private.key
```

Import key:
```bash
cat private.key | base64 -d | gpg --import -
```

Delete keys:
```bash
gpg --delete-secret-keys C12BA9B9AC50B47C2EC87B5A3767E58D5D276494
gpg --delete-keys C12BA9B9AC50B47C2EC87B5A3767E58D5D276494
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
