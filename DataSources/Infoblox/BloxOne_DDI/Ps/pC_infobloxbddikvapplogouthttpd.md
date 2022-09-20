#### Parser Content
```Java
{
Name = infoblox-bddi-kv-app-logout-httpd
  ParserVersion = v1.0.0
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ httpd: """, """]: Logout - -""", """ip=""", """group=""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}\S+)\s""",
    """: ({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """ip=({src_ip}[A-Fa-f:\d.]+)""",
    """group=({group_name}.+?)\s+(\w+=|$)""",
# trigger_event is removed
    """\d\d\dZ\s*\[({user}[^\]:]+)\]:"""
  ]


}
```