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
     """"Success":\s*({result}[^",}]+)""",
     """"ServiceName":"({service_name}[^@"]+)"""",
     """"UserIp":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
# cid is removed
     """"timestamp":"({time}[^"]+)""",
     """"UserId":\s*"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
     """"EventType":"({event_category}[^"]+)""",
     """"aid":"({aid}[^"]+)"""
     """"cid":"({cid}[^"]+)"""
  ]
  DupFields = [event_name->operation]


}
```