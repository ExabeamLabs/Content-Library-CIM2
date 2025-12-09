#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-login-fail-expiredpassword"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
""": expired password for user"""
"""sshd["""
  ]
  Fields = [
"""({host}[\w.\-]+)\s+sshd\["""
"""expired password for user ({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)) \(({failure_reason}[^\)]+?)\)"""
"""\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
  ]
  ParserVersion = "v1.0.0"


}
```