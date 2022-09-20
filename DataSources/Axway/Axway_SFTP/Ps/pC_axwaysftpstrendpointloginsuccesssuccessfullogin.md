#### Parser Content
```Java
{
Name = axway-sftp-str-endpoint-login-success-successfullogin
  Vendor = Axway
  Product = Axway SFTP
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """user:INFO""", """SSH: Successful login on""", """Username:""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s({src_ip}[\dA-Fa-f.:]+)""",
    """({event_name}Successful login)""",
    """Successful login on\s*\[?({dest_ip}[a-fA-F\d.:]+)\]?""",
    """Username:\s*"+({user}[^"]+)""",
    """({auth_package}SSH)"""
  ]
  ParserVersion = "v1.0.0"


}
```