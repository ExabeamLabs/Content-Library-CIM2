#### Parser Content
```Java
{
Name = "unix-unix-kv-endpoint-login-fail-su"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
""" su: pam_unix(su:auth)"""
"""authentication failure;"""
  ]
  Fields = [
"""\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+su:"""
"""\Wruser=({account}[^\s]+)"""
"""\Wuser=({user}[^\s]+)"""
"""({result}failure)"""
  ]
  ParserVersion = "v1.0.0"


}
```