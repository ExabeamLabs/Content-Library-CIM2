#### Parser Content
```Java
{
Name = unix-unix-kv-user-create-success-useradd
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """new user:""", """useradd""", """UID""" ]
  Fields = [
"""\d\d:\d\d:\d\d ({host}[\w.\-]+)\suseradd""",
"""\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[\+\-][^\s]+)""",
"""(\s|T)\d\d:\d\d:\d\d(\.?\S+)? ({host}[\w.\-]+)\suseradd""",
"""new user: name\\*=({account_name}[^,]+),""",
"""new user: .+?UID\\*=({account_id}[^,]+),""",
  ]
  DupFields = [ "host->src_host", "account_name->dest_user" ]


}
```