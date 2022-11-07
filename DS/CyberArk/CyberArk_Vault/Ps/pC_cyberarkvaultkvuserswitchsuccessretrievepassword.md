#### Parser Content
```Java
{
Name = cyberark-vault-kv-user-switch-success-retrievepassword
  Vendor = CyberArk
  Product = CyberArk Vault
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [  """;UsuarioCyberArk="""", """;Accion="Retrieve password"""", """;Safe="""" ]
  Fields = [
    """\w+\s+\d+\s+\d\d:\d\d:\d\d ({host}[\w\-.]+)""",
    """;Evento="({event_code}\d+)""",
    """;IP_Origen="({src_ip}[A-Fa-f:\d.]+)""",
    """;Usuario="({dest_user}[^\s"]+)""",
    """;IP="({dest_ip}[A-Fa-f:\d.]+)""",
    """;Safe="({safe_value}[^"]+)""",
    """;GatewayStation="(|({gateway_station}[^"]+))""",
    """;UsuarioCyberArk="({user}[^\s";]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```