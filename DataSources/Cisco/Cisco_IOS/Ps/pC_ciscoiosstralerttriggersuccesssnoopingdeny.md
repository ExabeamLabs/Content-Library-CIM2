#### Parser Content
```Java
{
Name = cisco-ios-str-alert-trigger-success-snoopingdeny
  Vendor = Cisco
  Product = Cisco IOS
  ParserVersion = v1.0.0
  TimeFormat = "HH:mm:ss 'UTC' EEE MMM dd yyyy"
  Conditions = [ """%SW_DAI-4-DHCP_SNOOPING_DENY""", """ARPs""" ]
  Fields = [
    """\/({time}\d\d:\d\d:\d\d\sUTC\s\w{3}\s\w{3}\s\d{1,2}\s\d{4})""",
    """\(\[[^\/]+\/({src_ip}[a-fA-F\d:.]+)\/[^\/]+\/({dest_ip}[a-fA-F\d:.]+)""",
    """({event_name}DHCP_SNOOPING_DENY)"""
  ]
  DupFields = [ "event_name->alert_name" ]


}
```