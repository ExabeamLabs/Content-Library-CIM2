#### Parser Content
```Java
{
Name = nagios-n-str-app-notification-serviceflappingalert
  ParserVersion = v1.0.0
  Vendor = Nagios
  Product = Nagios
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ nagios:""", """SERVICE FLAPPING ALERT:""" ]
  Fields = [
    """\W({host}[\w\-\.]+)\s+nagios:""",
    """SERVICE FLAPPING ALERT\s*:\s*({service_name}[^;]+);""",
# service_description is removed
    """SERVICE FLAPPING ALERT\s*:\s*([^;]+;){2}({service_state}[^;]+);""",
    """SERVICE FLAPPING ALERT\s*:\s*([^;]+;){3}\s*({additional_info}.+?)\s*$""",
    """({subtype}SERVICE FLAPPING ALERT)"""
  ]


}
```