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
"""expired password for user ({account}[^\(]+?) \(({failure_reason}[^\)]+?)\)"""
"""\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
  ]
  DupFields = [
"account->user"
  ]
  ParserVersion = "v1.0.0"


}
```