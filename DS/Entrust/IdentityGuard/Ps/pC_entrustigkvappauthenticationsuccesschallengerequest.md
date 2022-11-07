#### Parser Content
```Java
{
Name = entrust-ig-kv-app-authentication-success-challengerequest
  Vendor = Entrust
  Product = IdentityGuard
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """] [IG Audit """, """] User """ , """ challenge request was challenged.""", """ Certificate Authentication: """ ]
  Fields = [
    """\[({time}\d{4}-\d\d-\d\d \d\d:\d\d:\d\d)(\]|,\]|,\d+\])""",
# module is removed
    """({event_description}User (({email_address}[^\@\s]+@[^\s]+)|(({domain}[^\\\/]+)[\\\/]+)?({user}[^\s]+)) challenge request was challenged\.)""",
    """Application Name: ({app}[^\s,]+)""",
  ]


}
```