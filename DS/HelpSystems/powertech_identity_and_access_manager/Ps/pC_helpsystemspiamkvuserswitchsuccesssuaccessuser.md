#### Parser Content
```Java
{
Name = helpsystems-piam-kv-user-switch-success-suaccessuser
  ParserVersion = v1.0.0
  Vendor = HelpSystems
  Product = Powertech Identity and Access Manager
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
"""access.user.su""",
"""su_ok""",
"""Successful SU from user"""
  ]
  Fields = [
"""clientTime=\"*({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)Z\"*""",
"""\d\dZ\s+({host}[\w\-.]+)\s+su - su_ok""",
"""user=\"*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\"""",
"""touser=\"*({account}[^\"]+)\"""",
"""authHost=\"*({host}[^\"]+)\"""",
"""fromhost=\"*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\"""",
"""({event_code}su)"""
  ]
  DupFields = [ "host->dest_host" ]


}
```