#### Parser Content
```Java
{
Name = infoblox-bddi-kv-endpoint-login-success-loginallowed
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSZ"
  Conditions = [ """[INFOBLOX]""", """Login_Allowed""", """ip=""", """group=""" ]
  Fields = [
    """\w+\s+\d+\s+\d\d:\d\d:\d\d\s+\S+\s+({host}[\w\-.]+)\s+\S+\s+({time}\d+-\d+-\d+\s+\d+:\d+:\d+\.\d+Z)\s+\[({user}[^\s\]]+)\]:\s*({event_code}Login_Allowed)""",
    """ip=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """group=({group_name}.+?)\s+(\w+=|$)""",
  ]
  ParserVersion = "v1.0.0"


}
```