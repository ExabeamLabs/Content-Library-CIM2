#### Parser Content
```Java
{
Name = unix-unix-str-user-password-modify-success-chage
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy:MM:dd-HH:mm:ss"
  Conditions = [
"""changed password expiry for""",
"""chage["""
  ]
  Fields = [
"""({host}[\w.\-]+)\s+chage\["""
"""changed password expiry for ({account}\S+)"""
"""\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
  ]
  DupFields = [ "account->dest_user" ]


}
```