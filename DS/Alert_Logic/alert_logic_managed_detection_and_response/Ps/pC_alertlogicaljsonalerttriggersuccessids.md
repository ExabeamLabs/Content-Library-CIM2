#### Parser Content
```Java
{
Name = "alertlogic-al-json-alert-trigger-success-ids"
Vendor = "Alert Logic"
Product = "Alert Logic Managed Detection and Response"
TimeFormat = "epoch_sec"
Conditions = [
""""source_keyword":"""
"""IDS"""
""""account_deployments":"""
""""associatedEventCount":"""
]
ExtractionType = json
Fields = [
  """exa_json_path=$.generator.time,exa_field_name=time""",
  """exa_json_path=$.generator.hostName,exa_regex=({host}[\w\-.]+)""",
  """exa_json_path=$.victims[0],exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """exa_json_path=$.attacker[0],exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_json_path=$.incidentId,exa_field_name=alert_id""",
  """exa_json_path=$.incident.summary,exa_regex=({alert_name}[^"]+?)\s+from [A-Fa-f:\d.]+""",
  """exa_json_path=$..threatRating,exa_field_name=alert_severity"""
  """exa_json_path=$.incident.type,exa_field_name=alert_type""",
  """exa_json_path=$.observable.facts_url,exa_field_name=additional_info""",
]
ParserVersion = "v1.0.0"


}
```