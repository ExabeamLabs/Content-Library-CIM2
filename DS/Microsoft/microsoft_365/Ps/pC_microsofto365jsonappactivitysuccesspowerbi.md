#### Parser Content
```Java
{
Name = "microsoft-o365-json-app-activity-success-powerbi"
ExtractionType = json
Vendor = "Microsoft"
Product = "Microsoft 365"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """Workload"""
  """"PowerBI""""
  """"ActivityId":"""
]
Fields = [
  """exa_json_path=$.CreationTime,exa_field_name=time"""
  """exa_json_path=$.Workload,exa_field_name=app"""
  """exa_json_path=$.ObjectId,exa_field_name=object"""
  """exa_json_path=$.Operation,exa_field_name=operation"""
  """exa_json_path=$.UserId,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """exa_json_path=$.ClientIP,exa_field_name=src_ip"""
  """exa_json_path=$.ipAddress,exa_field_name=src_ip"""
  """exa_json_path=$.UserAgent,exa_field_name=user_agent"""
  """exa_regex="DatasetName":\s*"({data_set_name}[^"]+)"""
  """exa_json_path=$.Workload,exa_field_name=resource"""
  """exa_json_path=$.IsSuccess,exa_field_name=result"""
  """exa_json_path=$.Activity,exa_field_name=event_name"""
  """exa_json_path=$.ActivityId,exa_field_name=activity_id"""
]
ParserVersion = "v1.0.0"


}
```