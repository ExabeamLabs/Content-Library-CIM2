#### Parser Content
```Java
{
Name = juniper-ps-cef-vpn-logout-success-terminated
  ParserVersion = v1.0.0
  Vendor = Juniper Networks
  Product = Pulse Secure
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
"""CEF"""
"""Session for user """
""" on host """
""" has been terminated."""
]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s-\s""",
    """\stime="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """\sfw=({host}[\w\-\.]+)""",
    """({host}[\w\-\.]+)\s+(Juniper|PulseSecure):""",
    """PulseSecure:\s*\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d\s+\-\s+({dest_host}[\w\-.]+)""",
    """\s(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w\-\.]+))\s+(Juniper|PulseSecure):""",
    """Session for user\s+(({domain}[^\\]+)\\)?({user}.+?)\s+on host ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}) has been terminated"""
  ]


}
```