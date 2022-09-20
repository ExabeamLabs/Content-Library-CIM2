#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-app-login-success-appiname-1
  Vendor = Check Point 
  Product = NGFW
  TimeFormat = "ddMMMyyyy HH:mm:ss"
  Conditions = [ """CP_FireWall:""", """ProductName: Application Control;""", """appi_name""" ]
  Fields = [
    """CP_FireWall:\s+({time}\d+\w{3}\d+\s+\d+:\d+:\d+)(\s+\S+){4}\s+({host}[^\s]+)""",
    """;\s*appi_name:\s+({app}[^;]+);""",
    """;\s*web_client_type:\s+(Other: )?({user_agent}.+?);\s*($|web_server_type:)""",
    """\sdst:\s+({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\ssrc:\s+({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
  ]
  ParserVersion = v1.0.0


}
```