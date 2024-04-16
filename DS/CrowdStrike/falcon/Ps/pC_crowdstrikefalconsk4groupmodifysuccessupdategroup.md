#### Parser Content
```Java
{
Name = crowdstrike-falcon-sk4-group-modify-success-updategroup
  Product = Falcon
  ParserVersion = v1.0.0
  Conditions = [ """"event-name":""", """"audit-event"""", """"OperationName":"update_group"""" ]

crowdstrike-app-activity = {
    Vendor = CrowdStrike
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Fields = [
      """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
      """"OperationName":"({operation}[^"]+)""",
      """"UserId":\s*"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-]{1,40}\$?))"""",
      """"UserIp":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """"ServiceName":\s*"({app}[^"]+)""",
      """src-account-name":"({account_name}[^"]+)""",
      """src-account-id":"({account_id}[^"]+)""",
      """src-endpoint":"({endpoint}[^"]+)""",
      """"aid":"({aid}[^"]+)"""
    
}
```