#### Parser Content
```Java
{
Name = "okta-amfa-json-group-member-add-success-active"
Vendor = "Okta"
Product = "Okta Adaptive MFA"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
ExtractionType = json
Conditions = [
""""credentials":"""
""""provider":"""
""""type": "ACTIVE_DIRECTORY""""
""""status": "ACTIVE""""
]
Fields = [
   """exa_json_path=$.profile.employeeNumber,exa_field_name=account_id""",
   """exa_json_path=$.status,exa_field_name=event_name"""
   """exa_json_path=$.profile.title,exa_field_name=group_name""",
   """exa_json_path=$.profile.department,exa_field_name=group_type""",
   """exa_json_path=$.lastUpdated,exa_field_name=time"""
   """exa_json_path=$.profile.samAccountName,exa_field_name=user""",
   """exa_json_path=$.profile.email,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-]{1,40}\$?))""",
   """exa_json_path=$.profile.displayName,exa_regex="+:\s*"+({domain}[^\s\\"]+)\\+({user}[\w\.\-]{1,40}\$?)""",
]
ParserVersion = "v1.0.0"


}
```