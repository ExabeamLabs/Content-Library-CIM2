#### Parser Content
```Java
{
Name = "okta-amfa-json-app-login-fail-signinfailure"
 Vendor = "Okta"
 Product = "Okta Adaptive MFA"
 TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
 ExtractionType = json
 Conditions = [
   """Sign-in Failure"""
   """"published":"""
 ]
 Fields = [
   """exa_json_path=$.published,exa_field_name=time""",
   """exa_json_path=$.actors[*].ipAddress,exa_field_name=src_ip""",
   """exa_json_path=$.actors[*].login,exa_regex=(?:(({user}[\w\.\-]{1,40})@({domain}[^\s"]+?\.corp))|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))"""
   """exa_json_path=$.actors[1].id,exa_field_name=user_agent"""
   """exa_json_path=$.action.message,exa_field_name=failure_reason""",
   """exa_json_path=$.action.message,exa_regex=Sign-(I|i)n Failed\s*-\s*({failure_reason}[^"]+)""",
    ]
 ParserVersion = "v1.0.0"


}
```