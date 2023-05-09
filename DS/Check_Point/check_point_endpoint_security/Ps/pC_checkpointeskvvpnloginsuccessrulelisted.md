#### Parser Content
```Java
{
Name = checkpoint-es-kv-vpn-login-success-rulelisted
    ParserVersion = v1.0.0
  Vendor = Check Point
  Product = Check Point Endpoint Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """A rule was listed when the Windows Firewall started""", """Check Point""" ]
  Fields = [
    """Rule Name:\s*({rule}[^:]+?)("|\w+:)""",
    """Rule ID:\s*(\{|\s)({rule_id}[\w-]+)""",
    """({event_name}A rule was listed when the Windows Firewall started)"""
  ]


}
```