#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-app-notification-success-streamstarted
  Vendor = "CrowdStrike"
  Product = "Falcon"
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  ExtractionType = json
  Conditions = [
  """"EventType":"""
  """"Event_AuthActivityAuditEvent""""
  """"OperationName":"streamStarted""""
]
Fields = [
     """"OperationName":"({operation}({event_name}[^"]+))""",
     """"Success":\s*({result}[^",}]+)""",
     """"ServiceName":"({service_name}[^@"]+)"""",
     """"UserIp":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
     """"timestamp":"({time}[^"]+)""",
     """"UserId":\s*"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
     """"EventType":"({event_category}[^"]+)""",
     """"cid":"({cid}[^"]+)"""
     """exa_json_path=$.OperationName,exa_field_name=event_name""",
     """exa_json_path=$.OperationName,exa_field_name=operation""",
     """exa_json_path=$.Success,exa_field_name=result""",
     """exa_json_path=$.ServiceName,exa_field_name=service_name""",
     """exa_json_path=$.UserIp,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
     """exa_json_path=$.timestamp,exa_field_name=time""",
     """exa_regex="UserId":\s*"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
     """exa_json_path=$.EventType,exa_field_name=event_category""",
     """exa_json_path=$.cid,exa_field_name=cid""",
  ]


}
```