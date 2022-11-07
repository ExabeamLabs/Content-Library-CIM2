#### Parser Content
```Java
{
Name = crowdstrike-falcon-sk4-app-login-success-validateentitlement
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "epoch_sec"
  Conditions = [ """"eventType":""", """"AuthActivityAuditEvent"""", """"OperationName":""", """"validateEntitlementsHmac"""" ]
  Fields = [
    """"eventCreationTime":\s*({time}\d{10})""",
    """"timestamp":"({time}\d{10})"""",
    """"UTCTimestamp":({time}\d{10})""",
    """"UserId":\s*"({email_address}[^"@]+@({email_domain}[^"@]+))"""",
    """"UserId":\s*"({user}[^"@]+)"""",
    """"UserIp":\s*"({src_ip}[^"]+)""",
    """"ServiceName":\s*"({app}[^"]+)""",
    """"Success":\s*({result}[^",]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```