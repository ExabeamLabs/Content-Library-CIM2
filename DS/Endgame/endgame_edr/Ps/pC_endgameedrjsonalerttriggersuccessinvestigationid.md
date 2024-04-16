#### Parser Content
```Java
{
Name = "endgame-edr-json-alert-trigger-success-investigationid"
Vendor = "Endgame"
Product = "Endgame EDR"
TimeFormat = ["yyyy-MM-dd HH:mm:ssZ", "yyyy-MM-dd HH:mm:ss"]
ExtractionType = json
Conditions = [
"""investigation_id"""
""""doc_type": "alert""""
"""origination_task_id"""
]
Fields = [
  """exa_json_path=$..triggering_fact_array[0].serial_event_id,exa_field_name=alert_id"""
  """exa_json_path=$..pid,exa_field_name=process_id"""
  """exa_json_path=$..sha256,exa_field_name=hash_sha256"""
  """exa_json_path=$..process_name,exa_field_name=process_name"""
  """exa_json_path=$..user_name,exa_field_name=user"""
  """exa_json_path=$..timestamp_utc,exa_field_name=time"""
  """exa_json_path=$..parent_process_path,exa_field_name=parent_process_path"""
  """exa_json_path=$..original_file_name,exa_field_name=file_name"""
  """exa_json_path=$..user_sid,exa_field_name=user_sid"""
  """exa_json_path=$..parent_process_name,exa_field_name=parent_process_name"""
  """exa_regex="process_path\":\s*\"({process_path}({process_dir}.*?)(\\+({process_name}[^\\\"]+?))?)\""""
  """exa_json_path=$..user_domain,exa_field_name=domain"""
  """exa_json_path=$..md5,exa_field_name=hash_md5"""
  """exa_json_path=$..opcode,exa_field_name=opcode"""
  """exa_json_path=$..command_line,exa_field_name=process_command_line"""
  """exa_json_path=$..rule_id,exa_field_name=rule_id"""
  """exa_json_path=$..event_type_human,exa_field_name=event_name"""
  """exa_json_path=$..rule_name,exa_field_name=alert_name"""
  """exa_json_path=$.severity,exa_field_name=alert_severity"""
  """exa_json_path=$..hostname,exa_field_name=src_host"""
  """exa_json_path=$..ip_address,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_json_path=$..operating_system,exa_field_name=os"""
]
ParserVersion = "v1.0.0"


}
```