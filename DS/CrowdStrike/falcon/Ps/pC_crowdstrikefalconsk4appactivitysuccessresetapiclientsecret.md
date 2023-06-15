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
    """"UserIp":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"OperationName":"({operation}[^"]+)"""",
    """"((?i)EventType)":"({event_name}[^"]+)"""",
    """"UserId":"({email_address}[^@]+@[^.]+\.[^"]+)"""",
    """"Success":({result}[^,"]+),""",
    """"ServiceName":"({service_name}[^"]+)"""",
    """"AuditKeyValues":\[({additional_info}[^]]+)"""
  ]


}
```