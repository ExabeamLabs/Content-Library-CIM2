#### Parser Content
```Java
{
Name = juniper-ps-kv-app-login-success-loginsuccess
  Vendor = Juniper Networks
  Product = Pulse Secure
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """"AUT22670:""", """Login succeeded for""" ]
  Fields = [
    """\sfw=({host}[\w\-\.]+)""",
    """\w+\s*\d+\s*\d\d:\d\d:\d\d\s+({host}[\w.\-]+)\s*\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d""",
    """\stime="+({time}\d+-\d+-\d+ \d+:\d+:\d+).+?user""",
    """src=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s""",
    """user=({user}.+?)\s+realm=""",
    """realm="+({app}[^"]+)""",
    """agent="+({user_agent}[^"]+)"""",
  ]
  ParserVersion = "v1.0.0"


}
```