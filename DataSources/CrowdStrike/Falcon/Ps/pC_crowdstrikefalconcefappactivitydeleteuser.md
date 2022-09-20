#### Parser Content
```Java
{
Name = crowdstrike-falcon-cef-app-activity-deleteuser
  ParserVersion = "v1.0.0"
  Conditions = [ """"eventType":""", """"AuthActivityAuditEvent"""", """"OperationName":""", """"deleteUser"""" ]
  Fields =  ${CrowdStrikeParsersTemplates.crowdstrike-app-activity.Fields} [
    """"eventCreationTime":({time}\d{10})""",
    """"eventCreationTime":\s*({time}\d{10})""",
    """"UserId":\s*"({email_address}[^"@]+@[^"@]+)"""",
    """"UserId":\s*"({user}[^"@]+)"""",
    """"UserIp":\s*"({src_ip}[^"]+)""",
    """"ServiceName":\s*"({app}[^"]+)""",
    """"Success":\s*({result}[^",]+)""",
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
    """"aip":"({src_ip}[A-Fa-f:\d.]+)""",
    """suser=(system|({user}[^\s]+))""",
    """"Success":({result}true|false)""",
    """"UserId":"({email_address}[^@]+@({email_domain}[^"]+))""",
  
}
```