#### Parser Content
```Java
{
Name = juniper-ps-str-http-session-success-request
  ParserVersion = v1.0.0
  Vendor = Juniper Networks
  Product = Juniper Pulse Secure
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
""" PulseSecure:"""
""" Host: """
""", Request: """
]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+Z)\s+(::ffff:)?({host}[\w\-.]+)\s+PulseSecure:""",
    """PulseSecure:.+?({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)\s+\-\s+(::ffff:)?({host}[\w\-.]+)""",
    """PulseSecure:.*?\[(::ffff:)?({src_ip}[A-Fa-f:\d.]+)\]\s*\d+\(({realm}[^\)]+)\)\s*\[({role}[^\]]+)\]""",
    """PulseSecure:.*?\[(::ffff:)?({src_ip}[a-fA-F:\d.]+)\]\s+(({domain}[^\\]+)\\)?(?:({email_address}[^@\s]+@[^@\s]+)|({user}[^\s]+))\(({realm}[^\)]+)?""",
    """\WRequest:\s*({method}[^\s"]+)\s+({uri_path}\/[^",\s]*)""",
    """\WHost:\s*({web_domain}[^\s",:]+)""",
    """\w+\s+\d+\s+\d+:\d+:\d+\s+(::ffff:)?({firewall}[A-Fa-f:\d.]+)\s"""
  ]


}
```