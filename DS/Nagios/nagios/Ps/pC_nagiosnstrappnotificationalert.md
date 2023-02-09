#### Parser Content
```Java
{
Name = nagios-n-str-app-notification-alert
  Vendor = Nagios
  Product = Nagios
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ nagios:""", """SERVICE ALERT:""" ]
  Fields = [
    """\W({host}[\w\-\.]+)\s+nagios:""",
    """SERVICE ALERT\s*:\s*({service_name}[^;]+);""",
# service_description is removed
    """SERVICE ALERT\s*:\s*([^;]+;){2}({service_state}[^;]+);""",
# state_type is removed
# state_count is removed
    """SERVICE ALERT\s*:\s*([^;]+;){5}({additional_info}.+?)\s*$""",
    """({subtype}SERVICE ALERT)"""
  ]


}
```