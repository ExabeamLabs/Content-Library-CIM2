#### Parser Content
```Java
{
Name = okta-amfa-mix-app-login-fail-suspiciousactivity
    Vendor = Okta
    Product = Okta Adaptive MFA
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [ """Suspicious Activity""",""""published":""", """"objectType""""]
    Fields = [
      """"published":\s*"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)""",
      """"ipAddress":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """({app}Okta)""",
      """destinationServiceName({app}[^=]+?)\s*\w+=""",
      """AppInstance[^\}\{]+displayName":\s*"({app}[^"\}\{]+)"""",
      """\{[^\{]+?displayName":\s*"({app}[^"]+?)\s*"[^\}\{]+AppInstance""",
      """({alert_name}Suspicious Activity)[^=]+?objectType":\s*"({alert_type}[^"]+)"""",
      """message":\s*"({additional_info}[^"]+)"""",
      """message"*:\s*"*[^"]+?user:\s*(({email_address}[^"@]+@[^"@]+)|({user}[^"]+))""",
      """suser=((?i)(anonymous|system)|({email_address}[^@\s]+@({domain}[^\s@]+))|(({=domain}[^\\\s]+)\\+)?({user}[^\s]+))""",
      """({operation}(?i)(Sign-in Failed))""",
      """({result}Failed)""",
      """"targets":\s*\[\{[^\{\}]*?"displayName":\s*"({full_name}[^",\s]+\s+[^",]+)"[^\{\}]*?"objectType":\s*"User"""",
      """"targets":\s*\[\{[^\{\}]*?"objectType":\s*"User"[^\{\}]*?"displayName":\s*"({full_name}[^",]+\s+[^",]+)"""",
      """"targets"":\s*\[\{[^\{\}]*?""objectType"":\s*""User""[^\{\}]*?""displayName"":\s*""({last_name}[^,"]+),\s*({first_name}[^,"\}\]]+)"""",
    ]
        ParserVersion = "v1.0.0"
    DupFields = [ "additional_info->failure_reason" ]


}
```