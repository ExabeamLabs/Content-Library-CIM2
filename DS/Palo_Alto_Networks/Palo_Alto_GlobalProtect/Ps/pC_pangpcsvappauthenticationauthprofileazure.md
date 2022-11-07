#### Parser Content
```Java
{
Name = pan-gp-csv-app-authentication-authprofileazure
  Vendor = Palo Alto Networks
  Product = Palo Alto GlobalProtect
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  ParserVersion = v1.0.0
  Conditions = [
    """,SYSTEM,auth,""",
    """AUTH_PROFILE_AZURE"""
  ]
  Fields = [
    """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+\d+,({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+),""",
    """(c|C)lient '({src_ip}[A-Fa-f:\d.]+)""",
    """for user\s*'({email_address}[^']+)"""
    ]


}
```