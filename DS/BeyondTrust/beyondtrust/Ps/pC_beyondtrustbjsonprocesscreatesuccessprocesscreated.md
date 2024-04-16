#### Parser Content
```Java
{
Name = beyondtrust-b-json-process-create-success-processcreated
  Vendor = BeyondTrust
  Product = BeyondTrust
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"process_name":"""",""""vendor_product":"Beyondtrust Privilege Management"""", """"process_start_time":"""" ]
  Fields = [
  """exa_json_path=$.Processes.process_start_time,exa_field_name=time"""
  """exa_json_path=$.Processes.process_id,exa_field_name=process_id"""
  """exa_json_path=$.Processes,exa_regex=process_path":"({process_path}({process_dir}[^"]+(\\|\/)+)?({process_name}[^"]+))""""
  """exa_json_path=$.Processes.process,exa_field_name=process_command_line"""
  """exa_json_path=$.Processes.action,exa_field_name=action"""
  """exa_json_path=$.Processes.user,exa_regex=({user}[\w\.\-]{1,40}\$?)"""
  """exa_json_path=$.Processes.dest,exa_regex=({dest_host}[\w\-\.]+)"""
  """exa_json_path=$.Processes.user_id,exa_field_name=user_sid"""
  """exa_json_path=$.Processes.description,exa_field_name=additional_info"""
  """exa_json_path=$.Processes.parent_process,exa_regex=({parent_process_path}({parent_process_dir}[^"]+(\\|\/)+)?({parent_process_name}[^"]+))"""
  """exa_json_path=$.Processes.parent_process_id,exa_field_name=parent_process_id"""
  ]
  ParserVersion = "v1.0.0"


}
```