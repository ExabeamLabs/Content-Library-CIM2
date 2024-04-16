#### Parser Content
```Java
{
Name = okta-amfa-json-app-login-fail-signinfailed
  Vendor = Okta
  Product = Okta Adaptive MFA
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """EventDetails":""", """Sign-in Failed""", """"DisplayName":"""]
   ExtractionType = json
    Fields = [
      """exa_json_path=$.result.EventDetails,exa_field_name=failure_reason""",
      """exa_json_path=$.result.EventDetails,exa_regex=Sign-(I|i)n Failed\s*-\s*({failure_reason}[^"]+)""",
      """exa_json_path=$.result.IPAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
      """exa_json_path=$.result.user,exa_field_name=email_address""",
      """exa_json_path=$.result.Source,exa_field_name=additional_info""",
      """exa_json_path=$.result.Source,exa_regex=\[({additional_info}[^\]]+)"""
      """exa_json_path=$.result.Host,exa_field_name=host""",
      """exa_regex=({app}(o|O)kta)""",
      """exa_json_path=$.result.DisplayName,exa_field_name=full_name"""
      """exa_json_path=$.result.DisplayName[:1],exa_field_name=full_name""",
  ]
  ParserVersion = "v1.0.0"


}
```