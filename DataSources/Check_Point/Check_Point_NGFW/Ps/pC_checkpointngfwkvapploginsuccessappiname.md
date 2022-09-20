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
    """;user:\s+(?:.+?\()({user}[^\)]+)\)""",
    """;appi_name:\s+({app}[^;]+);""",
    """;web_client_type:\s+(Other: )?({user_agent}.+?)(;\s*$|;web_server_type:)""",
    """\sdst:\s+({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\ssrc:\s+({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
  ]


}
```