#### Parser Content
```Java
{
Name = axway-gateway-str-endpoint-login-success-successfullogin
  Vendor = Axway
  Product = Axway Gateway
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """user:INFO""", """SSH: Successful login on""", """Username:""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """({event_name}Successful login)""",
    """Successful login on\s*\[?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\]?""",
    """Username:\s*"+({user}[^"]+)""",
    """({auth_package}SSH)"""
  ]
  ParserVersion = "v1.0.0"


}
```