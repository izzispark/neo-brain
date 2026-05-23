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

### Encrypted Password (admin)

```
gAAAAABqEfJvyFlaz43ET5qT7emvOLVItsVsOiZ7zbkSFIliqMXQ6Ag6V9dRicLwhzfPtPa7ofEA-C0wd7xbsRogJ7Zix8KC_Ld1_xQoY4mEA13Qi-5zAIk=
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
password = fernet.decrypt("gAAAAABqEfJvyFlaz43ET5qT7emvOLVItsVsOiZ7zbkSFIliqMXQ6Ag6V9dRicLwhzfPtPa7ofEA-C0wd7xbsRogJ7Zix8KC_Ld1_xQoY4mEA13Qi-5zAIk=".encode()).decode()
print(password)
```

## Service Info

| Field | Value |
|-------|-------|
| URL | https://auth.izzispark.cloud |
| Admin user | neo |
| Admin email | neo@izzispark.cloud |
| Zitadel version | v4.15.0 |
| Deployed | 2026-05-23 |

## Related

- [[Projects/zitadel-migration|Zitadel Migration]]
- [[knowledge/03-hot-swaps|03 Hot Swaps]]
