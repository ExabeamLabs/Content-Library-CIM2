#### Parser Content
```Java
{
Name = "crowdstrike-falcon-json-app-notification-success-streamstopped"
  Vendor = "CrowdStrike"
  Product = "Falcon"
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  Conditions = [
  """"EventType":"""
  """"Event_AuthActivityAuditEvent""""
  """"OperationName":"streamStopped""""
  ]
  Fields = [
    """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""""
    """"UTCTimestamp":({time}\d{10})"""
    """"UserId":\s*"({email_address}[^"@]+@[^"@]+)"""",
    """"UserId":\s*"({user}[^"@]+)"""",
    """"ServiceName":\s*"({app}[^"]+)""",
    """"Success":\s*({result}[^",}]+)""",
    """"OperationName":"({event_name}[^"]+)"""
    """"EventType":"({event_category}[^"]+)"""
    """"aid":"({aid}[^"]+)"""
  ]
  DupFields = [event_name->operation]


}
```