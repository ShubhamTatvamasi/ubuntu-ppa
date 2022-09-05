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
gpg --export-secret-keys 2F37395FAB5B384875BAB01FA711441AA2FF1C95 | base64 > private.key
```

Import key:
```bash
cat private.key | base64 -d | gpg --import -
```

Delete keys:
```bash
gpg --delete-secret-keys 2F37395FAB5B384875BAB01FA711441AA2FF1C95
gpg --delete-keys 2F37395FAB5B384875BAB01FA711441AA2FF1C95
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
