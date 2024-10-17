#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-app-login-success-appiname
  ParserVersion = v1.0.0
  Vendor = Check Point
  Product = Check Point NGFW
  TimeFormat = "ddMMMyyyy HH:mm:ss"
  Conditions = [ """product: Application Control;""", """appi_name""" ]
  Fields = [
    """\s({host}[^\s]+)\s+product:""",
    """\s({time}\d+\w{3}\d+ \d+:\d+:\d+)""",
    """;user:\s+(?:.+?\()({user}[\w\.\-\!\#\^\~]{1,40}\$?)\)""",
    """;appi_name:\s+({app}[^;]+);""",
    """;web_client_type:\s+(Other: )?({user_agent}.+?)(;\s*$|;web_server_type:)""",
    """\sdst:\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\ssrc:\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  ]


}
```