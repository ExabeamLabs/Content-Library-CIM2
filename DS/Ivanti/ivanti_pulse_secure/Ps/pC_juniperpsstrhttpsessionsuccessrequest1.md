#### Parser Content
```Java
{
Name = juniper-ps-str-http-session-success-request-1
  ParserVersion = v1.0.0
  Vendor = Ivanti
  Product = Ivanti Pulse Secure
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
    """\Wuser=({user}[\w\.\-]{1,40}\$?)""",
    """\Wproto=({protocol}[^\s"]+)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wfw=({firewall}[A-Fa-f:\d.]+)""",
    """\Wrealm="({realm}[^"]+)""",
    """\Wroles="({role}[^"]+)""",
    """\WRequest:\s*({method}[^\s"]+)\s+({uri_path}\/[^",\s]*)""",
    """\WHost:\s*({web_domain}[^\s",:]+)"""
  ]


}
```