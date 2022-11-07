#### Parser Content
```Java
{
Name = nagios-n-str-endpoint-notification-hostalert
  ParserVersion = v1.0.0
  Vendor = Nagios
  Product = Nagios
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ nagios:""", """HOST ALERT:""" ]
  Fields = [
    """\W({host}[\w\-\.]+)\s+nagios:""",
# server_hostname is removed
# host_state is removed
# state_type is removed
# state_count is removed
    """HOST ALERT\s*:\s*([^;]+;){4}({additional_info}.+?)\s*$""",
    """({subtype}HOST ALERT)"""
  ]


}
```