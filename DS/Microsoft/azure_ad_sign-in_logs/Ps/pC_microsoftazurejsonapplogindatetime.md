#### Parser Content
```Java
{
Name = "microsoft-azure-json-app-login-datetime"
Vendor = "Microsoft"
Product = "Azure AD Sign-In Logs"
TimeFormat = "epoch"
ExtractionType = json
Conditions = [ """"signinDateTimeInMillis":""", """"loginStatus": """", """"mfaAuthDetail":""" ]
Fields = [
  """exa_json_path=$.signinDateTimeInMillis,exa_field_name=time""",
  """exa_json_path=$.ipAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_json_path=$.loginStatus,exa_field_name=result""",
  """exa_json_path=$.mfaResult,exa_field_name=additional_info""",
  """exa_json_path=$.signinErrorCode,exa_field_name=error_code""",
  """exa_json_path=$.userDisplayName,exa_regex=({first_name}[^,"]+),\s*({last_name}[^,"]+)"""
  """exa_json_path=$.appDisplayName,exa_field_name=app""",
  """exa_json_path=$.userPrincipalName,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)))\s*""",
  """exa_json_path=$.failureReason,exa_field_name=failure_reason,exa_match_expr=!InList(toLower($.failureReason), 'null')"""
]
ParserVersion = "v1.0.0"


}
```