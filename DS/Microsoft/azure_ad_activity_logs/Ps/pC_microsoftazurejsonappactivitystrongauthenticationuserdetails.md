#### Parser Content
```Java
{
Name = "microsoft-azure-json-app-activity-strongauthenticationuserdetails"
Vendor = "Microsoft"
Product = "Azure AD Activity Logs"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
ExtractionType = json
Conditions = [ """"activityDisplayName":""", """"Update user"""", """"operationType":""", """"Update"""", """"activityDateTime":""", """StrongAuthenticationUserDetails""", """VoiceOnlyPhoneNumber""" ]
Fields = [
  """exa_json_path=$..activityDateTime,exa_field_name=time""",
  """exa_json_path=$..result,exa_field_name=result""",
  """exa_json_path=$..activityDisplayName,exa_field_name=event_name""",
  """exa_json_path=$..operationType,exa_field_name=operation""",
  """exa_json_path=$..initiatedBy.user.id,exa_field_name=user_id""",
  """exa_json_path=$..initiatedBy.user.userPrincipalName,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)))\s*""",
  """exa_json_path=$..initiatedBy.user.userPrincipalName,exa_regex=({email_address}({user}[\w\.\-\!\#\^\~]{1,40}\$?)@[^\.\"]+\.[^\"]+)"""
  """exa_json_path=$..targetResources[*].userPrincipalName,exa_regex=(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[^@",\s]+))"""
  """exa_json_path=$..targetResources[*].userPrincipalName,exa_regex=({dest_user}[^@\"]+)"""
  """exa_json_path=$.resourceId,exa_field_name=object""",
 """exa_json_path=$..targetResources[*].modifiedProperties[*].newValue,exa_regex=\"\[({additional_info}\{[\\]?\"PhoneNumber[^]]+)"""
]
ParserVersion = "v1.0.0"


}
```