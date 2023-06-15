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
    """' from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """({event_name}Pfauth not performed for user)"""
    ]


}
```