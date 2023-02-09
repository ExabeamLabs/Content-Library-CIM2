#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-app-login-success-appiname-1
  Vendor = Check Point 
  Product = Check Point NGFW
  TimeFormat = "ddMMMyyyy HH:mm:ss"
  Conditions = [ """CP_FireWall:""", """ProductName: Application Control;""", """appi_name""" ]
  Fields = [
    """CP_FireWall:\s+({time}\d+\w{3}\d+\s+\d+:\d+:\d+)(\s+\S+){4}\s+({host}[^\s]+)""",
    """;\s*appi_name:\s+({app}[^;]+);""",
    """;\s*web_client_type:\s+(Other: )?({user_agent}.+?);\s*($|web_server_type:)""",
    """\sdst:\s+({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\ssrc:\s+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  ]
  ParserVersion = v1.0.0


}
```