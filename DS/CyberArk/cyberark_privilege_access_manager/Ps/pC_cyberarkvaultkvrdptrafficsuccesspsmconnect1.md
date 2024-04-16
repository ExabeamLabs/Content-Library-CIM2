#### Parser Content
```Java
{
Name = cyberark-vault-kv-rdp-traffic-success-psmconnect-1
  Conditions = [ """%CYBERARK:""", """Message="PSM Connect"""", """;Safe=""" ]
  Fields = ${CyberArkParsersTemplates.s-cyberark-events.Fields}[
    """;UserName ="(|(({domain}[^\s\\"]+)\\+)?({account}[^\s\\"]+))"""",
    """;LogonDomain="(|[\d\.]+|({account_domain}[^"]+?))"""",
  ]
  ParserVersion = v1.0.0

s-cyberark-events {
  Vendor = CyberArk
  Product = CyberArk Privilege Access Manager
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ","MMM dd HH:mm:ss"]
  Fields = [
    """({time}(\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ|\w+\s+\d\d\s+\d\d:\d\d:\d\d)) \S+ %CYBERARK""",
    """\d\d:\d\d:\d\d(Z)? ({host}[\w\-.]+) %CYBERARK""",
    """({app}CYBERARK)""",
    """;Message="(|({operation}[^"]+?))\s*"""",
    """MessageID="({event_code}\d+)""",
    """;Issuer="({user}[\w\.\-]{1,40}\$?)""",
    """;Station="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """;Safe="(|({safe_value}[^"]+))"""",
    """;DeviceType="(|({dest_service_name}[^"]+))"""",
    """;Address="(|(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\:({dest_port}\d+))?|({dest_host}[\w\-.]+)))""""
  
}
```