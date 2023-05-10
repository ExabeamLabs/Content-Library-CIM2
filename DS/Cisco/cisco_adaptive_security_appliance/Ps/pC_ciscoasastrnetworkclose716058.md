#### Parser Content
```Java
{
Name = cisco-asa-str-network-close-716058
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  ParserVersion = v1.0.0
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%ASA-""", """-716058""" ]
  Fields = [
    """({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d):\s*%ASA\-({priority}\d+)\-({event_code}\d+)""",
    """Group <({group_name}[^>]+)>""",
    """User <({user}[^>@]+)(@({domain}[^>@]+))?>""",
    """IP <(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))""",
    """({event_name}AnyConnect session lost connection)"""
  ]


}
```