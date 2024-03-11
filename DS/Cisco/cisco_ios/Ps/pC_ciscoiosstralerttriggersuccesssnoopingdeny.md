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
    """\(\[[^\/]+\/({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\/[^\/]+\/({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """({event_name}DHCP_SNOOPING_DENY)"""
  ]
  DupFields = [ "event_name->alert_name" ]


}
```