#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-user-modify-success-checkpoint
  ParserVersion = v1.0.0
  Vendor = Check Point
  Product = Check Point NGFW
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """A change was made to the Windows Firewall exception list""", """Check Point""" ]
  Fields = [
    """Rule Name:\s*({rule}[^:]+?)("|\w+:)""",
    """Rule ID:\s*(\{|\s)({rule_id}[\w-]+)""",
    """({event_name}A change was made to the Windows Firewall exception list)"""
  ]


}
```