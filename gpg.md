# GPG

### Setup

Generate new key:
```bash
gpg --expert --full-gen-key
```
> Elliptic curve keys are not supported. Create `RSA and RSA` key.

List your keys:
```bash
gpg --list-keys
```

Export private key:
```bash
gpg --output private.pgp --armor --export-secret-key shubhamtatvamasi@gmail.com
```

Convert Private key to base64:
```bash
# Encode
bash -c "echo '$(cat private.pgp | base64)'" > private.pgp
# Decode
bash -c "echo '$(cat private.pgp | base64 -d)'" > private.pgp
```

Import key:
```bash
gpg --import private.pgp
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
gpg --output public.pgp --armor --export shubhamtatvamasi@gmail.com
```
---

### decrypt messages

```bash
gpg --decrypt message.pgp
```

---

### sign

Sign Ubuntu Contract:
```bash
gpg --clearsign UbuntuCodeofConduct-2.0.txt
```

---

### Install

Install Gnu GPG tool:
```bash
brew install gnupg
```
> command is for macOS
