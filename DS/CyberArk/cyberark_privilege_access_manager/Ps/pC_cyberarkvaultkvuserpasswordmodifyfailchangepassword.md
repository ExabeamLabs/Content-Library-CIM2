#### Parser Content
```Java
{
Name = cyberark-vault-kv-user-password-modify-fail-changepassword
  Conditions = [ """%CYBERARK:""", """Message="CPM Change Password Failed"""", """;Safe=""" ]
  Fields = ${CyberArkParsersTemplates.s-cyberark-events.Fields} [
    """;UserName ="(|({dest_user}[^"]+))"""",
    """;LogonDomain="(|({dest_domain}[^"]+))"""",
  ]
  ParserVersion = "v1.0.0"

s-cyberark-events {
  Vendor = CyberArk
  Product = CyberArk Privilege Access Manager
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ","MMM dd HH:mm:ss"]
  Fields = [
    """({time}(\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ|\w+\s+\d\d\s+\d\d:\d\d:\d\d)) \S+ %CYBERARK""",
    """\d\d:\d\d:\d\d(Z)? ({dest_host}({host}[\w\-.]+)) %CYBERARK""",
    """({app}CYBERARK)""",
    """;Message="(|({operation}[^"]+?))\s*"""",
    """MessageID="({event_code}\d+)""",
    """;Issuer="({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """;Station="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """;Safe="(|({safe_value}[^"]+))"""",
    """;DeviceType="(|({dest_service_name}[^"]+))"""",
    """;Address="(|(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\:({dest_port}\d+))?|({dest_host}[\w\-.]+)))""""
  
}
```