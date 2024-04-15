#### Parser Content
```Java
{
Name = "proxysg-p-kv-endpoint-login-fail-invalidcreds"
Vendor = "ProxySG"
Product = "ProxySG"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""ProxySG:"""
"""LDAP: invalid credentials:"""
]
Fields = [
"""reason:\s*'({failure_reason}[^']+)"""
"""dn:\s*'CN=({full_name}[^=]+?),\s*({user_ou}OU=[^\s']+)"""
"""realm:\s*'({realm}[^']+)"""
]
ParserVersion = "v1.0.0"


}
```