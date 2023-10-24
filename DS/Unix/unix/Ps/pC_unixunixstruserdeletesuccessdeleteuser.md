#### Parser Content
```Java
{
Name = unix-unix-str-user-delete-success-deleteuser
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """delete user""", """userdel""" ]
  Fields = [
"""\d\d:\d\d:\d\d ({host}[\w.\-]+)\suserdel"""
"""\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[\+\-][^\s]+)""",
"""(\s|T)\d\d:\d\d:\d\d(\.?\S+)? ({host}[\w.\-]+)\suserdel""",
"""delete user \'({dest_user}[^']+)\'"""
  ]
  DupFields = [ "host->dest_host", "dest_user->account_name" ]


}
```