#### Parser Content
```Java
{
Name = ipswitch-moveitdmz-str-app-logout-dmzsignoff
  Vendor = IPSwitch
  Product = MoveIt DMZ
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [""" Sign Off""","""MOVEitDMZ""" ]
  Fields = [
    """\s\d\d:\d\d:\d\d\s({host}[^\s]+)"""
    """\sIPAddress:\s*({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})""",
    """User\s'(({email_address}[^@]+@[^']+)|Automation|({full_name}[^']+))?'\s\(({user}[^\)]+)?\)""",
    """\s:\s+({operation}[^,]+),\s+ID:""",
    """\sUsername:\s*({user}[^,]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```