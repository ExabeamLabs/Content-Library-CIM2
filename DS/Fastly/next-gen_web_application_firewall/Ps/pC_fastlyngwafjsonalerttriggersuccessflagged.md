#### Parser Content
```Java
{
Name = "fastly-ngwaf-json-alert-trigger-success-flagged"
ExtractionType = json
ParserVersion = "v1.0.0"
Vendor = "Fastly"
Product = "Next-Gen Web Application Firewall"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [ """"eventType": "flag"""", """"agentAction": "blocked"""" , """"alertAction": "flagged"""" ,""""formattedTags":""" ]
Fields = [
  """exa_json_path=$.created,exa_field_name=time"""
  """exa_json_path=$.eventType,exa_field_name=operation"""
  """exa_json_path=$.msgData.agentAction,exa_field_name=action"""
  """exa_json_path=$.msgData.id,exa_field_name=alert_id"""
  """exa_json_path=$.msgData.detailLink,exa_field_name=url"""
  """exa_json_path=$.msgData.eventHost,exa_field_name=src_host"""
  """exa_json_path=$.msgData.ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_json_path=$.message,exa_field_name=alert_name"""
  """exa_json_path=$.attachments,exa_field_name=additional_info"""
  """exa_json_path=$.msgData.formattedTags,exa_field_name=alert_type"""
]


}
```