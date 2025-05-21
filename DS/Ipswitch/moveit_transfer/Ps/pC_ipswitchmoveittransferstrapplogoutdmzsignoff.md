#### Parser Content
```Java
{
Name = ipswitch-moveittransfer-str-app-logout-dmzsignoff
  Vendor = Ipswitch
  Product = MoveIt Transfer
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [""" Sign Off""","""MOVEitDMZ""" ]
  Fields = [
    """\s\d\d:\d\d:\d\d\s({host}[^\s]+)"""
    """\sIPAddress:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """User\s'(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|Automation|({full_name}[^']+))?'\s\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)?\)""",
    """\s:\s+({operation}[^,]+),\s+ID:""",
    """\sUsername:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
  ]
  ParserVersion = "v1.0.0"


}
```