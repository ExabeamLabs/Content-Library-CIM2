#### Parser Content
```Java
{
Name = crowdstrike-falcon-cef-app-activity-revokeuserroles
  ParserVersion = "v1.0.0"
  Conditions = [ """"eventType":""", """"AuthActivityAuditEvent"""", """"OperationName":""", """"revokeUserRoles"""" ]
  Fields =  ${CrowdStrikeParsersTemplates.crowdstrike-app-activity.Fields} [
    """"eventCreationTime":({time}\d{10})""",
    """"eventCreationTime":\s*({time}\d{10})""",
    """"UserId":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
    """"UserId":\s*"({user}[\w\.\-]{1,40}\$?)"""",
    """"UserIp":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"ServiceName":\s*"({app}[^"]+)""",
    """"Success":\s*({result}[^",}]+)""",
    """"OperationName":"({event_name}[^"]+)"""
]

crowdstrike-app-activity = {
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "epoch_sec"
  Fields = [
    """"timestamp":"({time}\d{10})""",
    """"OperationName":"({operation}[^"]+)""",
    """"event_simpleName":"({operation}[^"]+)""",
    """"aip":"({aip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """suser=(system|({user}[\w\.\-]{1,40}\$?))""",
    """"Success":({result}true|false)""",
    """"UserId":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """"aid":"({aid}[^"]+)""",
    """"event_platform":"({os}[^"]+)"""",
    """"cid":"({cid}[^"]+)"""
  
}
```