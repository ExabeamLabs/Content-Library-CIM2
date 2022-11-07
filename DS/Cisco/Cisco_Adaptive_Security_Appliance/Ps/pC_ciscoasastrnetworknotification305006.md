#### Parser Content
```Java
{
Name = cisco-asa-str-network-notification-305006
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """-305006""", """%ASA-""" ]
  Fields = [
    """({host}[\w\-.]+)\s+({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d):\s*""",
    """({time}\w+ \d+ \d+ \d\d:\d\d:\d\d)\s+({host}[\w\-.]+)""",
    """%ASA-({priority}\d+)""",
    """({event_code}305006)""",
    """({event_name}regular translation creation failed) for ({protocol}\w+) src ({src_interface}\S+?)\s*:\s*({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))(\(({domain}[^\\\/\s]+)[\\\/]({src_host}[^\\\/\s]+)\))? dst ({dest_interface}\S+?)\s*:\s*(({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+?))"""
  ]


}
```