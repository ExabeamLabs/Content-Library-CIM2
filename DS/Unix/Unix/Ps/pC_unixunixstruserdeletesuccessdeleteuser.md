#### Parser Content
```Java
{
Name = unix-unix-str-user-delete-success-deleteuser
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
"""delete user""",
"""userdel"""
  ]
  Fields = [
"""\d\d:\d\d:\d\d ({host}[\w.\-]+)"""
"""delete user \'({dest_user}[^']+)\'"""
  ]
  DupFields = [ "host->dest_host", "dest_user->account_name" ]


}
```