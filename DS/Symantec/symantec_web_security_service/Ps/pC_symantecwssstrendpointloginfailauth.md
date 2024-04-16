#### Parser Content
```Java
{
Name = "symantec-wss-str-endpoint-login-fail-auth"
Vendor = "Symantec"
Product = "Symantec Web Security Service"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""ProxySG:"""
"""Authentication failed from"""
]
Fields = [
"""Authentication failed from ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}): user '({user}[\w\.\-]{1,40}\$?)"""
"""\(realm ({realm}[^\)]+)"""
]
ParserVersion = "v1.0.0"


}
```