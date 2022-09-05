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
gpg --output private.key --armor --export-secret-key shubhamtatvamasi@gmail.com
```

Import key:
```bash
gpg --import private.key
cat private.key | base64 -d | gpg --import -
```

Delete keys:
```bash
gpg --delete-secret-keys shubhamtatvamasi@gmail.com
gpg --delete-keys shubhamtatvamasi@gmail.com
```

---

### keyserver

Upload your public key to: https://keyserver.ubuntu.com
```bash
gpg --send-keys 0F195430352D314080C96E67B76BE3858E1FDB4F
```

Get your Public Key
```bash
gpg --output public.key --armor --export shubhamtatvamasi@gmail.com
```
---

### Install

Install Gnu GPG tool:
```bash
brew install gnupg
```
> command is for macOS
