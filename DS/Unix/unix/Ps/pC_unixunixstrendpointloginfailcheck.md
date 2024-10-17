#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-login-fail-check"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
""" unix_chkpwd["""
"""]: password check failed for """
  ]
  Fields = [
"""\w{3}\s+\d+\s+\d+:\d+:\d+\s+(::ffff:)?({host}[\w\-.]+)\s+"""
"""password check failed for user \(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)\)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)\)"""
  ]
  ParserVersion = "v1.0.0"


}
```