#### Parser Content
```Java
{
Name = "crowdstrike-falcon-cef-app-login-success-assert-1"
Vendor = "CrowdStrike"
Product = "Falcon"
TimeFormat = "epoch_sec"
ExtractionType = json
Conditions = [
  """"eventType":"""
  """"AuthActivityAuditEvent""""
  """"OperationName":"""
  """"saml2Assert""""
]
Fields = [
  """"eventCreationTime":\s*({time}\d{10})"""
  """"timestamp":"({time}\d{10})""""
  """"UTCTimestamp":({time}\d{10})"""
  """"UserId":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""""
  """"UserIp":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"ServiceName":\s*"({app}[^"]+)"""
  """"Success":\s*({result}[^",}]+)"""
  """"OperationName":\s*"({operation}[^",]+)"""
  """exa_json_path=$.metadata.eventCreationTime,exa_field_name=time""",
  """exa_json_path=$..timestamp,exa_field_name=time""",
  """exa_json_path=$..UTCTimestamp,exa_field_name=time""",
  """exa_json_path=$.event.UserId,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """exa_json_path=$.event.UserIp,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_json_path=$..ServiceName,exa_field_name=app""",
  """exa_json_path=$..Success,exa_field_name=result""",
  """exa_json_path=$..OperationName,exa_field_name=operation"""

]
ParserVersion = "v1.0.0"


}
```