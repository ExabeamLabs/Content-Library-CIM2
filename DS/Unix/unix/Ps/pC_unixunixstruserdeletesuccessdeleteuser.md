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
"""({time}\w+\s\d+\s\d\d:\d\d:\d\d)? ({dest_host}({host}[\w.\-]+))\suserdel"""
"""\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[\+\-][^\s]+)""",
"""(\s|T)\d\d:\d\d:\d\d(\.?\S+)? ({dest_host}({host}[\w.\-]+))\suserdel""",
"""delete user \'({account_name}({dest_user}[^']+))\'"""
"""\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
  ]


}
```