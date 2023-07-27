#### Parser Content
```Java
{
Name = cyberark-pam-kv-app-activity-fileoperations
  Vendor = CyberArk
  Product = Cyberark Privilege Access Management
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """%CYBERARK:""", """;Safe=""" ]
  Fields = [
    """({time}\d\d\d\d\d\-\d\d-\d\dT\d\d:\d\d:\d\dZ) \S+ %CYBERARK""",
    """\d\d:\d\d:\d\d(Z)? ({host}[\w\-.]+) %CYBERARK""",
    """MessageID="({event_code}\d+)""",
    """\d\d:\d\d:\d\d(Z)? ({app}[^\s]+) %CYBERARK:""",
    """({app}CYBERARK)""",
    """;Message="({operation}[^"]+)""",
    """;Issuer="({user}[\w\.\-]{1,40}\$?)""",
    """;Station="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """;File="({file_path}[^"]+)""",
    """;File="({file_dir}[^"]+?)[^\\"]+"""",
    """;File="[^"]*?[^"]+\\({file_name}[^"]+)""",
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