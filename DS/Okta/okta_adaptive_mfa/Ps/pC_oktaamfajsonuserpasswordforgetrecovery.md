#### Parser Content
```Java
{
Name = okta-amfa-json-user-password-forget-recovery
Vendor = Okta
Product = Okta Adaptive MFA
ParserVersion = "v1.0.0"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
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
]


}
```