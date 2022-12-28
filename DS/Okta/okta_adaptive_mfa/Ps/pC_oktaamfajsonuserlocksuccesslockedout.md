#### Parser Content
```Java
{
Name = okta-amfa-json-user-lock-success-lockedout
  Vendor = Okta
  Product = Okta Adaptive MFA
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"credentials": {"provider":""", """"type": "ACTIVE_DIRECTORY"""", """"status": "LOCKED_OUT"""" ]
  Fields = [
     """"employeeNumber":\s*"({account_id}[^"]+)"""",
     """"status":\s*"({event_name}[^"]+)"""",
     """"title":\s*"({group_name}[^"]+)"""",
     """"department":\s*"({group_type}[^"]+)"""",
     """"created":\s*"({time}[^"]+)"""",
     """"displayName"+:\s*"+({domain}[^\s\\"]+)\\+({user}[^\s"]+)"""
     """"samAccountName":\s*"({user}[^"]+)"""",
     """"email":\s*"({email_address}[^@"\s]+@({email_domain}[^@"\s]+))""""
  ]
  ParserVersion = "v1.0.0"


}
```