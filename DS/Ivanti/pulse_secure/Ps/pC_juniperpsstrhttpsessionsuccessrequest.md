#### Parser Content
```Java
{
Name = juniper-ps-str-http-session-success-request
  ParserVersion = v1.0.0
  Vendor = Ivanti
  Product = Pulse Secure
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
""" PulseSecure:"""
""" Host: """
""", Request: """
]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+Z)\s+(::ffff:)?({host}[\w\-.]+)\s+PulseSecure:""",
    """PulseSecure:.+?({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)\s+\-\s+(::ffff:)?({host}[\w\-.]+)""",
    """PulseSecure:.*?\[(::ffff:)?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\s*\d+\(({realm}[^\)]+)\)\s*\[({role}[^\]]+)\]""",
    """PulseSecure:.*?\[(::ffff:)?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\s+(({domain}[^\\]+)\\)?(?:({email_address}[^@\s]+@[^@\s]+)|({user}[^\s]+))\(({realm}[^\)]+)?""",
    """\WRequest:\s*({method}[^\s"]+)\s+({uri_path}\/[^",\s]*)""",
    """\WHost:\s*({web_domain}[^\s",:]+)""",
    """\w+\s+\d+\s+\d+:\d+:\d+\s+(::ffff:)?({firewall}[A-Fa-f:\d.]+)\s"""
  ]


}
```