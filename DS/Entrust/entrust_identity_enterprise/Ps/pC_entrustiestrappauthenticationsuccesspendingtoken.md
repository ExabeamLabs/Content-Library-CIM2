#### Parser Content
```Java
{
Name = entrust-ie-str-app-authentication-success-pendingtoken
  Vendor = Entrust
  Product = Entrust Identity Enterprise
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """] [IG Audit """, """] User """ , """ authenticated with pending token.""", """ State: """ ]
  Fields = [
    """\[({time}\d{4}-\d\d-\d\d \d\d:\d\d:\d\d)(\]|,\]|,\d+\])""",
# module is removed
    """({event_description}User (({email_address}[^\@\s]+@[^\s]+)|(({domain}[^\\\/]+)[\\\/]+)?({user}[\w\.\-]{1,40}\$?)) authenticated with pending token\.)""",
  ]


}
```