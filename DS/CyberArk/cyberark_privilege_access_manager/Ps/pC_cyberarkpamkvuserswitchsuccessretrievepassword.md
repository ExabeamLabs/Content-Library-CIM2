#### Parser Content
```Java
{
Name = cyberark-pam-kv-user-switch-success-retrievepassword
  Vendor = CyberArk
  Product = "CyberArk Privilege Access Manager"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [  """;UsuarioCyberArk="""", """;Accion="Retrieve password"""", """;Safe="""" ]
  Fields = [
    """\w+\s+\d+\s+\d\d:\d\d:\d\d ({host}[\w\-.]+)""",
    """;Evento="({event_code}\d+)""",
    """;IP_Origen="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """;Usuario="({dest_user}[^\s"]+)""",
    """;IP="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """;Safe="({safe_value}[^"]+)""",
    """;GatewayStation="(|({gateway_station}[^"]+))""",
    """;UsuarioCyberArk="({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
  ]
  DupFields = [ "dest_user->account" ]
  ParserVersion = "v1.0.0"


}
```