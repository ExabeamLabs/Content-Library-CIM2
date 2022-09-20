#### Parser Content
```Java
{
Name = infoblox-bddi-str-app-logout-success-group
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSZ"
  Conditions = [ """[INFOBLOX]""", """Logout""", """ip=""", """group=""" ]
  Fields = [
    """\w+\s+\d+\s+\d\d:\d\d:\d\d\s+\S+\s+({host}[\w\-.]+)\s+\S+\s+({time}\d+-\d+-\d+\s+\d+:\d+:\d+\.\d+Z)\s+\[({user}[^\s\]]+)\]:\s*({event_code}Logout)""",
    """ip=({src_ip}[A-Fa-f:\d.]+)""",
    """group=({group_name}.+?)\s+(\w+=|$)""",
  ]
  ParserVersion = "v1.0.0"


}
```