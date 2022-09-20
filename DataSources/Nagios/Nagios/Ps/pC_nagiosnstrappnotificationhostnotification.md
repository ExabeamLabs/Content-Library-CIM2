#### Parser Content
```Java
{
Name = nagios-n-str-app-notification-hostnotification
  ParserVersion = v1.0.0
  Vendor = Nagios
  Product = Nagios
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ nagios:""", """HOST NOTIFICATION:""" ]
  Fields = [
    """\W({host}[\w\-\.]+)\s+nagios:""",
# notified_user is removed
# server_hostname is removed
# host_state is removed
# notification_handler is removed
    """HOST NOTIFICATION\s*:\s*([^;]+;){4}({additional_info}.+?)\s*$""",
    """({subtype}HOST NOTIFICATION)"""
  ]


}
```