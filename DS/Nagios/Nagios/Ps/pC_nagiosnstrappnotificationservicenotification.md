#### Parser Content
```Java
{
Name = nagios-n-str-app-notification-servicenotification
  ParserVersion = v1.0.0
  Vendor = Nagios
  Product = Nagios
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ nagios:""", """SERVICE NOTIFICATION:""" ]
  Fields = [
    """\W({host}[\w\-\.]+)\s+nagios:""",
# notified_user is removed
    """SERVICE NOTIFICATION\s*:\s*([^;]+;){1}({service_name}[^;]+);""",
# service_description is removed
    """SERVICE NOTIFICATION\s*:\s*([^;]+;){3}({service_state}[^;]+);""",
# notification_handler is removed
    """SERVICE NOTIFICATION\s*:\s*([^;]+;){5}({additional_info}.+?)\s*$""",
    """({subtype}SERVICE NOTIFICATION)"""
  ]


}
```