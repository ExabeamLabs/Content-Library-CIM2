#### Parser Content
```Java
{
Name = nagios-n-str-app-notification-hostflappingalert
  ParserVersion = v1.0.0
  Vendor = Nagios
  Product = Nagios
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ nagios:""", """HOST FLAPPING ALERT:""" ]
  Fields = [
    """\W({host}[\w\-\.]+)\s+nagios:""",
# server_hostname is removed
# host_state is removed
    """HOST FLAPPING ALERT\s*:\s*([^;]+;){2}\s*({additional_info}.+?)\s*$""",
    """({subtype}HOST FLAPPING ALERT)"""
  ]


}
```