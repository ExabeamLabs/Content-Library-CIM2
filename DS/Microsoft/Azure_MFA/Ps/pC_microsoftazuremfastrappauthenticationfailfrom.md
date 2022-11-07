#### Parser Content
```Java
{
Name = microsoft-azuremfa-str-app-authentication-fail-from
  ParserVersion = v1.0.0  
  Vendor = Microsoft
  Product = Azure MFA
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ pfsvc: Pfauth not performed for user""", """' from """ ]
  Fields = [
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s({host}[^\s]+)\spfsvc:""",
    """user\s+'(({email_address}[^'@]+@[^'\s]+)|(({domain}[^\\\s']+)\\)?({user}[^\s']+))""",
    """' from ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """({event_name}Pfauth not performed for user)"""
    ]


}
```