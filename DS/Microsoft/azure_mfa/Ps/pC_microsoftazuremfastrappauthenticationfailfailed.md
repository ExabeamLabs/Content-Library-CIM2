#### Parser Content
```Java
{
Name = microsoft-azuremfa-str-app-authentication-fail-failed
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Azure MFA
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ pfsvc: Primary auth failed for user '""" ]
  Fields = [
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s({host}[^\s]+)\spfsvc:""",
    """user\s+'(({email_address}[^'@]+@[^'\s]+)|(({domain}[^\\\s']+)\\)?({user}[\w\.\-]{1,40}\$?))""",
    """({event_name}Primary auth failed for user)"""
    ]


}
```