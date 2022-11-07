#### Parser Content
```Java
{
Name = juniper-ps-str-http-session-success-request-2
  ParserVersion = v1.0.0
  Vendor = Juniper Networks
  Product = Pulse Secure
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
""" PulseSecure:"""
"""WebRequest completed,"""
]
  Fields = [
    """PulseSecure:.+?({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)\s+\-\s+(::ffff:)?({host}[\w\-.]+)""",
    """PulseSecure:.*?\[({src_ip}[a-fA-F:\d.]+)\]\s+(({domain}[^\\]+)\\)?(?:({email_address}[^@\s]+@[^@\s]+)|({user}[^\s]+))\(({realm}[^\)]+)?""",
    """WebRequest completed,\s*({method}[^\s]+)\s+\S+\s+({url}(({protocol}[\w]+):\/+)?({web_domain}[^\s:\\\/]+)(:({dest_port}\d+)\/+)?({uri_path}\/[^\s\?]+)?({uri_query}\?[^\s]+)?)\s+""",
    """\Wresult=({http_response_code}\d+)""",
    """\Wsent=({bytes_out}\d+)""",
    """\Wreceived=({bytes_in}\d+)""",
    """from\s(::ffff:)?({src_ip}[A-Fa-f\d:.]+)"""
  ]


}
```