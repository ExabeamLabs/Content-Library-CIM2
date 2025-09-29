#### Parser Content
```Java
{
Name = unix-unix-str-user-delete-success-deleteuser
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ","MMM dd HH:mm:ss"]
  Conditions = [ """delete user""", """userdel""" ]
  Fields = [
"""({time}\w+\s\d+\s\d\d:\d\d:\d\d)? ({host}[\w.\-]+)\suserdel"""
"""\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[\+\-][^\s]+)""",
"""(\s|T)\d\d:\d\d:\d\d(\.?\S+)? ({host}[\w.\-]+)\suserdel""",
"""delete user \'({dest_user}[^']+)\'"""
"""\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
  ]
  DupFields = [ "host->dest_host", "dest_user->account_name" ]


}
```