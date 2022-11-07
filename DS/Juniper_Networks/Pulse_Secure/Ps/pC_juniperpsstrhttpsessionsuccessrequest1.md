#### Parser Content
```Java
{
Name = juniper-ps-str-http-session-success-request-1
  ParserVersion = v1.0.0
  Vendor = Juniper Networks
  Product = Pulse Secure
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
""" PulseSecure:"""
""" Host: """
""", Request: """
"""user="""
]
  Fields = [
    """\s+({host}[\w\-.]+)\s+PulseSecure:""",
    """\Wtime="({time}\d+-\d+-\d+\s+\d+:\d+:\d+)""",
    """\Wuser=({user}[^\s"]+)""",
    """\Wproto=({protocol}[^\s"]+)""",
    """\Wsrc=({src_ip}[A-Fa-f:\d.]+)""",
    """\Wfw=({firewall}[A-Fa-f:\d.]+)""",
    """\Wrealm="({realm}[^"]+)""",
    """\Wroles="({role}[^"]+)""",
    """\WRequest:\s*({method}[^\s"]+)\s+({uri_path}\/[^",\s]*)""",
    """\WHost:\s*({web_domain}[^\s",:]+)"""
  ]


}
```