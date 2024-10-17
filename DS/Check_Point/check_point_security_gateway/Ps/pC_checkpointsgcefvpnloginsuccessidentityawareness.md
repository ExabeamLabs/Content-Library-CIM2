#### Parser Content
```Java
{
Name = checkpoint-sg-cef-vpn-login-success-identityawareness
  ParserVersion = v1.0.0
  Vendor = Check Point
  Product = Check Point Security Gateway
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Check Point|""", """act=IP Changed""", """product=Identity Awareness""" ]
  Fields = [
    """\Wrt=({time}\d{13})""",
    """\Wdvc=({host}[A-Fa-f:\d.]+)""",
    """\Wduser=({last_name}[^\,=]+),\s*({first_name}[^\(=]+?)\s*(\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)\))?\s+(\w+=|$)""",
    """\Wsntdom=({domain}[^\s]+)""",
    """\Worigin=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wsrc=({src_translated_ip}[A-Fa-f:\d.]+)""",
  ]


}
```