#### Parser Content
```Java
{
Name = unix-unix-kv-user-create-success-useradd
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """new user:""", """useradd""", """UID""" ]
  Fields = [
"""\d\d:\d\d:\d\d ({host}[\w.\-]+)\suseradd""",
"""new user: name=({account_name}[^,]+),""",
"""new user: .+?UID=({account_id}[^,]+),""",
  ]
  DupFields = [ "host->dest_host" ]


}
```