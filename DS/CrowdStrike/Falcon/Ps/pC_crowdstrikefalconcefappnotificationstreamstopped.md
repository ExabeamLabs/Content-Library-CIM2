#### Parser Content
```Java
{
Name = crowdstrike-falcon-cef-app-notification-streamstopped
  ParserVersion = v1.0.0
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """destinationServiceName =CrowdStrike""", """"OperationName":"streamStopped"""" ]
  Fields = [
     """"OperationName":"({event_name}[^"]+)""",
     """"Success":\s*({result}[^",]+)""",
     """"ServiceName":"({service_name}[^@"]+)"""",
     """"UserIp":\s*"({src_ip}[A-Fa-f:\d.]+)""",
# cid is removed
     """"timestamp":"({time}[^"]+)""",
     """"UserId":\s*"({user}[^"@]+)"""",
     """"EventType":"({event_category}[^"]+)"""
  ]
  DupFields = [event_name->operation]


}
```