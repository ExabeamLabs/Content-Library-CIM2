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
"""\Wuser=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))"""
"""({result}failure)"""
  ]
  ParserVersion = "v1.0.0"


}
```