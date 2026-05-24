---
date: 2026-05-23
updated: 2026-05-23
type: knowledge
tags: [credentials, zitadel, auth, security]
ai-first: true
stated: high
---

## For future Claude

Zitadel admin credentials — encrypted at rest. Decrypt before use. Never commit raw passwords to version control.

## Zitadel Admin — auth.izzispark.cloud

**Encryption:** Fernet (AES-128-CBC)
**Key derivation:** hex→base64 (see below)
**Encrypted at:** 2026-05-23
**Updated:** 2026-05-23 — new password with complexity compliance

### Encrypted Password (admin)

```
gAAAAABqEfkT7oCrlYlrRRWd-OO24omxO-5tP14USWAekyjXxH2lB7ZhafwzFcFNZF2p7Pnz4PL-BGdgpecHd-D2jUKGMK_SDQ==
```

### Key Derivation String

```
0718876553dec6ee0a9d4d075b0d1c178d2c327c0826bc1c62b2bf74463a29b1
```

### To Decrypt (Python)

```python
from cryptography.fernet import Fernet
import base64

key = base64.urlsafe_b64encode(bytes.fromhex("0718876553dec6ee0a9d4d075b0d1c178d2c327c0826bc1c62b2bf74463a29b1"))
fernet = Fernet(key)
password = fernet.decrypt("gAAAAABqEfkT7oCrlYlrRRWd-OO24omxO-5tP14USWAekyjXxH2lB7ZhafwzFcFNZF2p7Pnz4PL-BGdgpecHd-D2jUKGMK_SDQ==".encode()).decode()
print(password)
```

## Service Info

| Field | Value |
|-------|-------|
| URL | https://auth.izzispark.cloud |
| Admin user | neo |
| Admin email | neo@izzispark.cloud |
| Password | NzXk#2026mJpw! (encrypted above) |
| Zitadel version | v4.15.0 |
| Deployed | 2026-05-23 |

## Related

- [[Projects/zitadel-migration|Zitadel Migration]]
- [[knowledge/03-hot-swaps|03 Hot Swaps]]
