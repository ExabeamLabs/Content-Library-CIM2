#### Parser Content
```Java
{
Name = cyberark-vault-kv-app-activity-fileoperations
  Vendor = CyberArk
  Product = CyberArk Vault
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """%CYBERARK:""", """;Safe=""" ]
  Fields = [
    """({time}\d\d\d\d\d\-\d\d-\d\dT\d\d:\d\d:\d\dZ) \S+ %CYBERARK""",
    """\d\d:\d\d:\d\d(Z)? ({host}[\w\-.]+) %CYBERARK""",
    """MessageID="({event_code}\d+)""",
    """\d\d:\d\d:\d\d(Z)? ({app}[^\s]+) %CYBERARK:""",
    """;Message="({operation}[^"]+)""",
    """;Issuer="({user}[^"]+)""",
    """;Station="({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """;File="({file_path}[^"]+)""",
    """;File="({file_dir}[^"]+?)[^\"]+"""",
    """;File="[^"]*?({file_name}[^\"]+?)"""",
    """;File="[^"]*?\.({file_ext}[a-zA-Z]+?)";Safe=""",
    """;Safe="({safe_value}[^"]+)""",
    """;UserName ="({account}[^"]+)""",
    """;LogonDomain="({domain}[^"]+)""",
    """;DeviceType="({dest_service_name}[^"]+)"""
  ]
  DupFields=[ "file_name->object_value", "file_path->additional_info", "operation->access", "host->dest_host" ]
  ParserVersion = "v1.0.0"


}
```