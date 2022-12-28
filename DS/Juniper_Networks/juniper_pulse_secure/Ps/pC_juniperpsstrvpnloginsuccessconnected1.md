#### Parser Content
```Java
{
Name = juniper-ps-str-vpn-login-success-connected-1
  ParserVersion = v1.0.0
  Vendor = Juniper Networks
  Product = Juniper Pulse Secure
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
""": User with IP """
""" connected with """
"""VPN Tunneling:"""
]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s-\s""",
    """PulseSecure:\s*({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)\s+\-\s+(::ffff:)?({host}[\w\-.]+)""",
    """\s+(::ffff:)?({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w\-.]+)))\s+(Juniper|PulseSecure):""",
    """PulseSecure:\s*\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d\s+\-\s+(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w\-.]+))""",
    """\- \[({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\]\s+(({domain}[^\\]+)\\)?({user}[^\(]+)\(({realm}[^\)]+)?\)""",
    """: User with IP ({src_translated_ip}[A-Fa-f\d:.]+)"""
  ]
  DupFields = [ "user->account" ]


}
```