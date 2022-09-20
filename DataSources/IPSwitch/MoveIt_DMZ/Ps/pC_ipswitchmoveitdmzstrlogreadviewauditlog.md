#### Parser Content
```Java
{
Name = ipswitch-moveitdmz-str-log-read-viewauditlog
  Vendor = IPSwitch
  Product = MoveIt DMZ
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """MOVEitDMZ""", """View Audit Log"""]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)"""
    """\s\d\d:\d\d:\d\d\s({host}[^\s]+)""",
    """\sIPAddress:\s*({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})""",
    """User\s'(({email_address}[^@]+@[^']+)|Automation|({full_name}[^']+))?'\s\(({user}[^\)]+)?\)""",
    """\s:\s+({operation}[^,]+),\s+ID:""",
    """\sUsername:\s*(Automation|({user}[^,]+))""",
    """AgentBrand:\s+({browser}[^,]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```