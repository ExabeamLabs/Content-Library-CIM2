#### Parser Content
```Java
{
Name = "citrix-cgateway-str-vpn-authentication-success-succeededpolicy"
  Vendor = "Citrix"
  Product = "Citrix Gateway"
  TimeFormat = "MM/dd/yyyy:HH:mm:ss"
  Conditions = [ """ AAA Message """, """Succeeded policy for user""" ]
  Fields = [
    """({time}\d+\/\d+\/\d+:\d+:\d+:\d+)\s*(GMT\s*)?[\w\-\.]+\s*\S+\s*:""",
    """\s*(GMT)?\s*({src_host}({host}[^:\s]+))\s*\S+\s*:\s\w+\sAAA Message""",
    """\s:\s*({event_code}(\w+\s+){2}\w+)\s+""",
    """:\s*(\\)?"({event_name}.+)\s+for""",
    """\s+for\s*user\s*(({domain}[^\\\s]+)\\+)?(-|({email_address}[^@"\s]+@[^@"\s]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """\s*=\s*({auth_method}[^\s"]+)"?"""
    """\s*=\s*({auth_type}[^\s"]+)"?"""
  ]
  ParserVersion = "v1.0.0"


}
```