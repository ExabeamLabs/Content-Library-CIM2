#### Parser Content
```Java
{
Name = infoblox-bddi-kv-endpoint-login-success-loginallow
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """Login_Allowed""", """Remote""", """ip=""", """group=""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s+({host}[\w\-.]+)\s+""",
    """\s+\[({user}[\w\.\-\!\#\^\~]{1,40}\$?)\]:\s*({event_name}Login_Allowed)""",
    """ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """auth=({auth_method}[^\s]+)""",
    """Transfer status:\s({action}[^\s]+?)\s*$"""
    """group=({group_name}.+?)(\w+=|$)"""
  ]
  ParserVersion = "v1.0.0"


}
```