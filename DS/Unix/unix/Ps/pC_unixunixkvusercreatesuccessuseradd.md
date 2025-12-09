#### Parser Content
```Java
{
Name = unix-unix-kv-user-create-success-useradd
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ","MMM dd HH:mm:ss"]
  Conditions = [ """new user:""", """useradd""", """UID""" ]
  Fields = [
"""({time}\w+\s\d+\s\d\d:\d\d:\d\d)?\s*({src_host}({host}[\w.\-]+))\suseradd""",
"""\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[\+\-][^\s]+)""",
"""(\s|T)\d\d:\d\d:\d\d(\.?\S+)? ({src_host}({host}[\w.\-]+))\suseradd""",
"""new user: name\\*=({dest_user}({account_name}[^,]+)),""",
"""new user: .+?UID\\*=({account_id}[^,]+),""",
"""\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
  ]


}
```