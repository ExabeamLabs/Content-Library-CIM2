#### Parser Content
```Java
{
Name = "unix-unix-str-user-password-modify-success-changepasswd"
Vendor = "Unix"
Product = "Unix"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""changed password for"""
"""passwd:"""
]
Fields = [
"""({host}[\w.\-]+)\s+passwd:"""
"""changed password for '({account}[^']+)'"""
]
ParserVersion = "v1.0.0"


}
```