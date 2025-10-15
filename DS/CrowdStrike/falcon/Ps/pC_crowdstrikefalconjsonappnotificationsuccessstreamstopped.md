#### Parser Content
```Java
{
Name = "crowdstrike-falcon-json-app-notification-success-streamstopped"
  Vendor = "CrowdStrike"
  Product = "Falcon"
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  ExtractionType = json
  Conditions = [
  """"EventType":"""
  """"Event_AuthActivityAuditEvent""""
  """"OperationName":"streamStopped""""
  ]
  Fields = [
    """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""""
    """"UTCTimestamp":({time}\d{10})"""
    """"UserId":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
    """"UserId":\s*"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
    """"ServiceName":\s*"({app}[^"]+)""",
    """"Success":\s*({result}[^",}]+)""",
    """"OperationName":"({operation}({event_name}[^"]+))"""
    """"EventType":"({event_category}[^"]+)"""
    """"aid":"({aid}[^"]+)"""
    """exa_json_path=$.timestamp,exa_field_name=time""",
    """exa_json_path=$.UTCTimestamp,exa_field_name=time""",
    """exa_regex="UserId":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
    """exa_regex="UserId":\s*"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
    """exa_json_path=$.ServiceName,exa_field_name=app""",
    """exa_json_path=$.Success,exa_field_name=result"""
    """exa_json_path=$.OperationName,exa_field_name=event_name"""
    """exa_json_path=$.OperationName,exa_field_name=operation"""
    """exa_json_path=$.EventType,exa_field_name=event_category"""
    """exa_json_path=$.aid,exa_field_name=aid"""
  ]


}
```