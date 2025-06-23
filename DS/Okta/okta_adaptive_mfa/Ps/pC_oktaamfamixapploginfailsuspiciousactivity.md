#### Parser Content
```Java
{
Name = okta-amfa-mix-app-login-fail-suspiciousactivity
    Vendor = Okta
    Product = Okta Adaptive MFA
    ExtractionType = json
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Conditions = [ """Suspicious Activity""",""""published":""", """"objectType""""]
    Fields = [
      """exa_json_path=$.published,exa_field_name=time""",
      """exa_json_path=$.actors[:1].ipAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """exa_regex=({app}Okta)""",
      """exa_regex=({alert_name}Suspicious Activity)[^=]+?objectType":\s*"({alert_type}[^"]+)"""",
      """exa_json_path=$.action.message,exa_field_name=additional_info""",
      """exa_regex=({operation}(?i)(Sign-in Failed))""",
      """exa_regex=({result}Failed)""",
      """exa_json_path=$.targets[:1].displayName,exa_field_name=full_name""",
      """exa_json_path=$.targets[:1].displayName,exa_regex=({last_name}[^,"]+),\s*({first_name}[^,"\}\]]+)""",
      """exa_json_path=$.targets[:1].login,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
      """exa_regex=behaviors":"\{({more_info}[^\}]+)"""
    ]
    ParserVersion = "v1.0.0"
    DupFields = [ "additional_info->failure_reason" ]


}
```