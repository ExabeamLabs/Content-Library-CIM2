#### Parser Content
```Java
{
Name = helpsystems-piam-kv-user-switch-success-suaccessuser
  ParserVersion = v1.0.0
  Vendor = HelpSystems
  Product = Powertech Identity Access Manager (BoKs)
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
"""access.user.su""",
"""su_ok""",
"""Successful SU from user"""
  ]
  Fields = [
"""clientTime=\"*({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)Z\"*""",
"""\d\dZ\s+({host}[\w\-.]+)\s+su - su_ok""",
"""user=\"*({user}[^\"]+)\"""",
"""touser=\"*({dest_user}[^\"]+)\"""",
"""authHost=\"*({host}[^\"]+)\"""",
"""fromhost=\"*({dest_ip}[^\"]+)\"""",
"""({event_code}su)"""
  ]


}
```