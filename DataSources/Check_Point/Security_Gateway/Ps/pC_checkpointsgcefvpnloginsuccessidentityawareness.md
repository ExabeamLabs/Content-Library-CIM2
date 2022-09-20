#### Parser Content
```Java
{
Name = checkpoint-sg-cef-vpn-login-success-identityawareness
  ParserVersion = v1.0.0
  Vendor = Check Point
  Product = Security Gateway
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Check Point|""", """act=IP Changed""", """product=Identity Awareness""" ]
  Fields = [
    """\Wrt=({time}\d+)""",
    """\Wdvc=({host}[A-Fa-f:\d.]+)""",
    """\Wduser=({last_name}[^\,=]+),\s*({first_name}[^\(=]+?)\s*(\(({user}[^\s\)=]+)\))?\s+(\w+=|$)""",
    """\Wsntdom=({domain}[^\s]+)""",
    """\Worigin=({src_ip}[A-Fa-f:\d.]+)""",
    """\Wsrc=({src_translated_ip}[A-Fa-f:\d.]+)""",
  ]


}
```