#### Parser Content
```Java
{
Name = crowdstrike-falcon-sk4-app-activity-success-resetapiclientsecret
  Vendor = CrowdStrike
  Product = Falcon
  ParserVersion = v1.0.0
  TimeFormat = "epoch_sec"
  Conditions = [ """"OperationName":"ResetAPIClientSecret"""",""""ServiceName":"""",""""UserIp":"""" ]
  Fields = [
    """"UTCTimestamp":({time}\d{10})""",
    """"UserIp":"({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""",
    """"OperationName":"({operation}[^"]+)"""",
    """"((?i)EventType)":"({event_name}[^"]+)"""",
    """"UserId":"({email_address}[^@]+@[^.]+\.[^"]+)"""",
    """"Success":({result}[^,"]+),""",
    """"ServiceName":"({service_name}[^"]+)"""",
    """"AuditKeyValues":\[({additional_info}[^]]+)"""
  ]


}
```