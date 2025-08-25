# Code Changes for unix-unixauditd-kv-endpoint-authentication-success-cryptokeyuser (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| changed | Conditions | [' msg=', ' msg=audit(', ' res=', ' type=CRYPTO_KEY_USER'] | [' msg=', ' res=', 'CRYPTO_KEY_USER', 'audit'] |