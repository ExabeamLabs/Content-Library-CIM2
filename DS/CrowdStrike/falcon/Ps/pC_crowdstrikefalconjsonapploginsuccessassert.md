#### Parser Content
```Java
{
Name = "crowdstrike-falcon-json-app-login-success-assert"
Vendor = "CrowdStrike"
Product = "Falcon"
ExtractionType = json
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ", "epoch_sec","epoch"]
Conditions = [
  """"EventType":"""
  """"Event_AuthActivityAuditEvent""""
  """"OperationName":"""
  """"saml2Assert""""
]
Fields = [
  """exa_regex="eventCreationTime":\s*({time}\d{10})""",
  """exa_json_path=$.UTCTimestamp,exa_field_name=time""",
  """exa_json_path=$.timestamp,exa_field_name=time""",
  """exa_json_path=$.UserId,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
  """exa_json_path=$.UserIp,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """exa_json_path=$.ServiceName,exa_field_name=app""",
  """exa_json_path=$.Success,exa_field_name=result""",
  """exa_json_path=$.OperationName,exa_field_name=event_name"""
  """exa_json_path=$.cid,exa_field_name=cid"""
]
ParserVersion = "v1.0.0"


}
```