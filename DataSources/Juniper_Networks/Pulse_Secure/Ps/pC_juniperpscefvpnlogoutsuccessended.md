#### Parser Content
```Java
{
Name = juniper-ps-cef-vpn-logout-success-ended
  ParserVersion = v1.0.0
  Vendor = Juniper Networks
  Product = Pulse Secure
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
""": Session ended for user"""
""" user="""
]
  Fields = [
    """\stime="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""",
    """\sfw=({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w\-\.]+)))""",
    """({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|[\w\-\.]+)\s*(Juniper|PulseSecure):""",
    """PulseSecure:\s*({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)\s+\-\s+({host}[\w\-.]+)""",
    """\s+({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w-.]+)))\s+PulseSecure:""",
    """\suser=(({domain}[^\\]+)\\)?({user}[^\s]+)\s""",
    """src=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """with IP(?:v4 address)?\s+({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\ssent=({bytes_out}\d+)""",
    """\srcvd=({bytes_in}\d+)""",
    """\s(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))\s+(Juniper|PulseSecure):""",
    """duration=({session_duration}[^\s]+)\s+"""
  ]


}
```