#### Parser Content
```Java
{
Name = unix-unix-str-user-password-modify-success-keyring
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
"""couldn't change password for""",
"""keyring:"""
  ]
  Fields = [
"""({host}[\w.\-]+)\s+passwd:""",
"""couldn't change password for '({account}[^']+)""",
  ]


}
```