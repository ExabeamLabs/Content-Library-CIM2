# Code Changes for proxysg-p-kv-endpoint-login-fail-invalidcreds (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| removed_parser | N/A | {"Name": "proxysg-p-kv-endpoint-login-fail-invalidcreds", "Vendor": "Symantec", "Product": "Blue Coat ProxySG", "TimeFormat": "yyyy-MM-dd HH:mm:ss", "Conditions": ["ProxySG:", "LDAP: invalid credentials:"], "Fields": ["reason:\s*'({failure_reason}[^']+)", "dn:\s*'CN=({full_name}[^=]+?),\s*({user_ou}OU=[^\s']+)", "realm:\s*'({realm}[^']+)"], "ParserVersion": "v1.0.0"} | N/A |