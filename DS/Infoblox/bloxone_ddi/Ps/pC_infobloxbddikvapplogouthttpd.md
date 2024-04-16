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
    """ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """group=({group_name}.+?)\s+(\w+=|$)""",
# trigger_event is removed
    """\d\d\dZ\s*\[(({email_address}[^@\]]+@[^\.\]]+\.[^\]]+)|({user}[\w\.\-]{1,40}\$?))\]:""",
    """({event_name}Logout)"""
  ]


}
```