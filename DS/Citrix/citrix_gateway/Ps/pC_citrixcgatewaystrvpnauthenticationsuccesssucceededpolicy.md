#### Parser Content
```Java
{
Name = "citrix-cgateway-str-vpn-authentication-success-succeededpolicy"
  Vendor = "Citrix"
  Product = "Citrix Gateway"
  TimeFormat = "MM/dd/yyyy:HH:mm:ss"
  Conditions = [ """ AAA Message """, """Succeeded policy for user""" ]
  Fields = [
    """({time}\d+\/\d+\/\d+:\d+:\d+:\d+)\s*GMT""",
    """GMT\s*({host}[^:\s]+)""",
    """\s:\s*({event_code}(\w+\s+){2}\w+)\s+""",
    """:\s*(\\)?"({event_name}.+)\s+for""",
    """\s+for\s*user\s*(({domain}[^\\\s]+)\\+)?({user}[^\s]+)""",
    """\s*=\s*({auth_method}[^\s]+)"""
  ]
  DupFields = [ "host->src_host", "auth_method->auth_type" ]
  ParserVersion = "v1.0.0"


}
```