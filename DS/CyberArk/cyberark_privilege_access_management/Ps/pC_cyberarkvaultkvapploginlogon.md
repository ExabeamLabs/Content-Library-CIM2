#### Parser Content
```Java
{
Name = cyberark-vault-kv-app-login-logon
  Conditions = [ """%CYBERARK:""", """Message="Logon""", """;Safe=""" ]
  Fields = ${CyberArkParsersTemplates.s-cyberark-events.Fields} [
    """;CPMStatus="(|({result}[^"]+))"""",
    """;Reason="(|({failure_reason}[^"]+))""""
  ]
  DupFields=[ "host->dest_host" ]
  ParserVersion = v1.0.0

s-cyberark-events {
  Vendor = CyberArk
  Product = Cyberark Privilege Access Management
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ) \S+ %CYBERARK""",
    """\d\d:\d\d:\d\d(Z)? ({host}[\w\-.]+) %CYBERARK""",
    """({app}CYBERARK)""",
    """;Message="(|({operation}[^"]+?))\s*"""",
    """MessageID="({event_code}\d+)""",
    """;Issuer="({user}[^";]+)""",
    """;Station="({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """;Safe="(|({safe_value}[^"]+))"""",
    """;DeviceType="(|({dest_service_name}[^"]+))"""",
    """;Address="(|(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(\:({dest_port}\d+))?|({dest_host}[\w\-.]+)))""""
  
}
```