#### Parser Content
```Java
{
Name = openvpn-sslvpn-str-app-notification-ovpn
  Vendor = Open VPN
  Product = SSL VPN
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """[OVPN""", """] OUT""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d+)""",
    """(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec)\s\d+\s\d+:\d+:\d+\s\d+\s({user}[^\/]+)\/({src_ip}\d+.\d+.\d+.\d+):({src_port}\d+)""",
    """peer info: ({additional_info}[^']+)""",
    """(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec)\s\d+\s\d+:\d+:\d+\s\d+.*?({src_ip}\d+.\d+.\d+.\d+):({src_port}\d+).*?\s*({additional_info}[^']+)""",
  ]


}
```