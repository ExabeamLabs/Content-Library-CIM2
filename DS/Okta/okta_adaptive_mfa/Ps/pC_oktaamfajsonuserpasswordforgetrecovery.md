#### Parser Content
```Java
{
Name = okta-amfa-json-user-password-forget-recovery
Vendor = Okta
Product = Okta Adaptive MFA
ParserVersion = "v1.0.0"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
ExtractionType = json
Conditions = [ """"credentials": {"provider":""", """"type": "ACTIVE_DIRECTORY"""", """"status": "RECOVERY"""" ]
Fields = [
""""employeeNumber":\s*"({account_id}[^"]+)"""",
""""status":\s*"({event_name}[^"]+)"""",
""""title":\s*"({group_name}[^"]+)"""",
""""department":\s*"({group_type}[^"]+)"""",
"""lastUpdated":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)"""
""""displayName"+:\s*"+({domain}[^\s\\"]+)\\+({user}[\w\.\-]{1,40}\$?)"""
""""samAccountName":\s*"({user}[\w\.\-]{1,40}\$?)"""",
""""email":\s*"({email_address}[^@"\s]+@({email_domain}[^@"\s]+))""""
"""exa_json_path=$.employeeNumber,exa_field_name=account_id"""
"""exa_json_path=$.status,exa_field_name=event_name"""
"""exa_json_path=$.title,exa_field_name=group_name"""
"""exa_json_path=$.department,exa_field_name=group_type"""
"""exa_json_path=$.lastUpdated,exa_field_name=time"""
"""exa_regex="displayName"+:\s*"+({domain}[^\s\\"]+)\\+({user}[\w\.\-]{1,40}\$?)"""
"""exa_regex="samAccountName":\s*"({user}[\w\.\-]{1,40}\$?)""""
""""email":\s*"({email_address}[^@"\s]+@({email_domain}[^@"\s]+))""""
]


}
```