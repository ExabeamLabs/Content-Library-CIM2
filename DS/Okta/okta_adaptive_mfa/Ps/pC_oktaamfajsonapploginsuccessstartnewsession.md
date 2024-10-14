#### Parser Content
```Java
{
Name = okta-amfa-json-app-login-success-startnewsession
  Vendor = Okta
  Product = Okta Adaptive MFA
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  ExtractionType = json
  Conditions = [ """Start New Session""", """"tenantHost":""" ]
  Fields = [
    """exa_json_path=$.userAgent,exa_field_name=user_agent""",
    """exa_json_path=$.requestTime,exa_field_name=time""",
    """exa_json_path=$.systemAccount,exa_field_name=user""",
    """exa_json_path=$.tenantHost,exa_field_name=app""",
    """exa_json_path=$.activityAction,exa_field_name=operation""",
    """exa_json_path=$.target.descriptor,exa_regex=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*\/\s*({full_name}[^"]+)"""
    """exa_json_path=$.ipAddress,exa_field_name=src_ip"""
  ]
  ParserVersion = "v1.0.0"


}
```