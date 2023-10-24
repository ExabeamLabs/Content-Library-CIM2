#### Parser Content
```Java
{
Name = "crowdstrike-falcon-sk4-app-logout-streamstopped"
  Vendor = "CrowdStrike"
  Product = "Falcon"
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  Conditions = [""""eventType":""", """"AuthActivityAuditEvent"""", """"OperationName":""", """"streamStopped""""]
  Fields = [
    """"eventCreationTime":\s*({time}\d{10})""",
    """"UserId":\s*"({email_address}[^"@]+@[^"@]+)"""",
    """"UserId":\s*"({user}[\w\.\-]{1,40}\$?)"""",
    """"UserIp":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"ServiceName":\s*"({app}[^"]+)""",
    """"Success":\s*({result}[^",}]+)""",
    """"OperationName":"({event_name}[^"]+)"""
    ]


}
```