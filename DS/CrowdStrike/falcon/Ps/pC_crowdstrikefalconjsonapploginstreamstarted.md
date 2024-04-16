#### Parser Content
```Java
{
Name = "crowdstrike-falcon-json-app-login-streamstarted"
Vendor = "CrowdStrike"
Product = "Falcon"
ExtractionType = json
TimeFormat = "epoch_sec"
Conditions = [
  """"eventType":"""
  """"AuthActivityAuditEvent""""
  """"OperationName":"""
  """"streamStarted""""
]
Fields = [
  """exa_json_path=$.metadata.eventCreationTime,exa_field_name=time""",
  """exa_regex="timestamp":"({time}\d{10})"""",
  """exa_json_path=$.event.UTCTimestamp,exa_field_name=time""",
  """exa_json_path=$.event.UserId,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
  """exa_json_path=$.event.UserId,exa_field_name=user_id""",
  """exa_json_path=$.event.UserIp,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """exa_json_path=$.event.ServiceName,exa_field_name=app""",
  """exa_json_path=$.event.Success,exa_field_name=result""",
  """exa_json_path=$.event.OperationName,exa_field_name=operation"""
]
ParserVersion = "v1.0.0"


}
```