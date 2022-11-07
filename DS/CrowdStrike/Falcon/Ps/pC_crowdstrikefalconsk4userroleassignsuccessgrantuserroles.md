#### Parser Content
```Java
{
Name = crowdstrike-falcon-sk4-user-role-assign-success-grantuserroles
  Product = Falcon
  ParserVersion = v1.0.0
  Conditions = [ """"event-name":""", """"audit-event"""", """"OperationName":"grantUserRoles"""" ]

crowdstrike-app-activity = {
    Vendor = CrowdStrike
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Fields = [
      """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
      """"OperationName":"({operation}[^"]+)""",
      """"UserId":\s*"(({email_address}[^"@]+@({email_domain}[^"@]+))|({user}[^"]+))"""",
      """"UserIp":\s*"({src_ip}[^"]+)""",
      """"ServiceName":\s*"({app}[^"]+)""",
      """src-account-name":"({account_name}[^"]+)""",
      """src-account-id":"({account_id}[^"]+)""",
      """src-endpoint":"({endpoint}[^"]+)""",
    
}
```