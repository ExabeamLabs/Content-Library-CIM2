#### Parser Content
```Java
{
Name = amazon-awscloudtrail-json-app-activity-success-cloudtrailapicall
  Vendor = Amazon
  Product = AWS CloudTrail
  ExtractionType = json
  TimeFormat = "epoch"
  ParserVersion = v1.0.0
  Conditions = [ """"name":"CloudTrail"""", """"event_code":"AwsApiCall"""", """"category_name":""" ]
  Fields = [
  """exa_json_path=$.time,exa_field_name=time""",
  """exa_json_path=$.activity_name,exa_field_name=operation""",
  """exa_json_path=$.type_name,exa_field_name=operation_type""",
  """exa_json_path=$.category_name,exa_field_name=category""",
  """exa_json_path=$.status,exa_field_name=result""",
  """exa_json_path=$.action,exa_field_name=action""",
  """exa_json_path=$..event_code,exa_field_name=event_code""",
  """exa_json_path=$.status_code,exa_field_name=action""",
  """exa_json_path=$.cloud.provider,exa_field_name=provider_name""",
  """exa_json_path=$.cloud.region,exa_field_name=region""",
  """exa_json_path=$.cloud.account.uid,exa_field_name=user_id""",
  """exa_json_path=$.class_name,exa_field_name=class_name""",
  """exa_json_path=$.severity,exa_field_name=severity"""  
  """exa_json_path=$.src_endpoint.port,exa_field_name=src_port"""  
  """exa_json_path=$.src_endpoint.ip,exa_field_name=src_ip"""  
  """exa_json_path=$.src_endpoint.domain,exa_field_name=domain"""  
  """exa_json_path=$.dst_endpoint.port,exa_field_name=dest_port"""  
  """exa_json_path=$.dst_endpoint.ip,exa_field_name=dest_ip"""  
  """exa_json_path=$.disposition,exa_field_name=disposition"""  
  """exa_json_path=$.connection_info.direction,exa_field_name=direction"""
  """exa_json_path=$.actor.user.uid,exa_field_name=user_id"""
  """exa_json_path=$.actor.user.name,exa_field_name=user"""
  """exa_json_path=$.actor.user.type,exa_field_name=user_type"""
  """exa_json_path=$.http_request.user_agent,exa_field_name=user_agent"""
  ]


}
```