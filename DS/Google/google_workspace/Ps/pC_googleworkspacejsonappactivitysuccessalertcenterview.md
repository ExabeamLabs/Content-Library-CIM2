#### Parser Content
```Java
{
Name = google-workspace-json-app-activity-success-alertcenterview
ParserVersion = v1.0.0
Vendor = Google
Product = Google Workspace
ExtractionType = json
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
Conditions = [""""name":""", """ALERT_CENTER_VIEW"""",  """"etag"""" ]
Fields = [
  """exa_json_path=$.events..name,exa_field_name=event_name"""
  """exa_json_path=$.etag,exa_field_name=tag"""
  """exa_json_path=$.actor.email,exa_field_name=email_address"""
  """exa_json_path=$.id.customerId,exa_field_name=resource_id"""
  """exa_json_path=$.id.time,exa_field_name=time"""
  """exa_json_path=$.ipAddress,exa_field_name=src_ip"""
]


}
```