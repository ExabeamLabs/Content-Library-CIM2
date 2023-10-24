#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-app-notification-success-streamstarted
  Vendor = "CrowdStrike"
  Product = "Falcon"
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [
  """"EventType":"""
  """"Event_AuthActivityAuditEvent""""
  """"OperationName":"streamStarted""""
]
Fields = [
     """"OperationName":"({event_name}[^"]+)""",
     """"Success":\s*({result}[^",}]+)""",
     """"ServiceName":"({service_name}[^@"]+)"""",
     """"UserIp":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
     """"timestamp":"({time}[^"]+)""",
     """"UserId":\s*"({user}[\w\.\-]{1,40}\$?)"""",
     """"EventType":"({event_category}[^"]+)""",
     """"cid":"({cid}[^"]+)"""
  ]
  DupFields = [event_name->operation]


}
```