#### Parser Content
```Java
{
Name = infoblox-bddi-str-app-logout-success-group
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSZ"
  Conditions = [ """[INFOBLOX]""", """Logout""", """ip=""", """group=""" ]
  Fields = [
    """\w+\s+\d+\s+\d\d:\d\d:\d\d\s+\S+\s+({host}[\w\-.]+)\s+\S+\s+({time}\d+-\d+-\d+\s+\d+:\d+:\d+\.\d+Z)\s+\[({user}[\w\.\-]{1,40}\$?)\]:\s*({event_code}Logout)""",
    """ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """group=({group_name}.+?)\s+(\w+=|$)""",
  ]
  ParserVersion = "v1.0.0"


}
```