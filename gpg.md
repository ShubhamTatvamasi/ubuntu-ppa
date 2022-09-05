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
gpg --export-secret-keys BDA80C28141B91819D48CAF2A4C0B31C7875404B | base64 > private.key
```

Import key:
```bash
cat private.key | base64 -d | gpg --import -
```

Delete keys:
```bash
gpg --delete-secret-keys BDA80C28141B91819D48CAF2A4C0B31C7875404B
gpg --delete-keys BDA80C28141B91819D48CAF2A4C0B31C7875404B
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
