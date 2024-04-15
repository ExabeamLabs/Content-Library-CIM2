#### Parser Content
```Java
{
Name = "unix-unix-kv-endpoint-login-fail-passwd"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
""" passwd: pam_unix("""
"""authentication failure;"""
  ]
  Fields = [
"""\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+passwd:"""
"""\Wruser=({account}[^\s]+)"""
"""\Wuser=({user}[^\s]+)"""
"""({result}failure)"""
  ]
  ParserVersion = "v1.0.0"


}
```