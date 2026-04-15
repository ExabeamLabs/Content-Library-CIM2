#### Parser Content
```Java
{
Name = beyondtrust-b-json-process-create-success-ecs
  Conditions = [ """"agent":""", """"Type":"Process""", """"EPMWinMac":""", """AgentEventAudit""", """"code":"""" ]
  Fields = ${BeyondTrustParserTemplates.beyondtrust-json-epm-events.Fields} [
  """exa_json_path=$.process.parent.pid,exa_field_name=parent_process_id"""
  """exa_json_path=$.process.parent.command_line,exa_field_name=parent_process_command_line"""
  """exa_json_path=$.process.parent.executable,exa_regex=({parent_process_path}({parent_process_dir}[^"]+[\\]+)?({parent_process_name}[^"]+))"""
  """exa_json_path=$.process.start,exa_field_name=start_time"""
  """exa_json_path=$.process.pid,exa_field_name=process_id"""
  """exa_json_path=$.process.command_line,exa_field_name=process_command_line"""
  """exa_json_path=$.process.executable,exa_regex=({process_path}({process_dir}[^"]+[\\]+)?({process_name}[^"]+))"""
  """exa_json_path=$.file.extension,exa_field_name=file_ext"""
  """exa_json_path=$.file.owner,exa_field_name=file_owner"""
  """exa_json_path=$.file.directory,exa_field_name=file_dir"""
  """exa_json_path=$.file.path,exa_field_name=file_path"""
  """exa_json_path=$.file.name,exa_field_name=file_name"""
  """exa_json_path=$.file.hash.sha1,exa_field_name=hash_sha1"""
  """exa_json_path=$.file.hash.sha256,exa_field_name=hash_sha256"""
  """exa_json_path=$.file.hash.md5,exa_field_name=hash_md5"""
]
  ParserVersion = "v1.0.0"

beyondtrust-json-epm-events = {
  Vendor = BeyondTrust
  Product = BeyondTrust
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  start_timeFormat="yyyy-MM-dd'T'HH:mm:ssZ"
  Fields = [
    """exa_json_path=$.@timestamp,exa_field_name=time"""
    """exa_json_path=$..Event.Type,exa_field_name=event_category"""
    """exa_json_path=$..GroupId,exa_field_name=group_id"""
    """exa_json_path=$.host.hostname,exa_field_name=host"""
    """exa_json_path=$.host.os.name,exa_field_name=os"""
    """exa_json_path=$.host.os.version,exa_field_name=os_version"""
    """exa_json_path=$.host.ip[0],exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.host.domain,exa_field_name=src_domain"""
    """exa_json_path=$.event.reason,exa_field_name=result_reason"""
    """exa_json_path=$.event.code,exa_field_name=event_code"""
    """exa_json_path=$.event.action,exa_field_name=action"""
    """exa_json_path=$.event.outcome,exa_field_name=result"""
    """exa_json_path=$.user.domain,exa_field_name=domain"""
    """exa_json_path=$.user.name,exa_regex=({user}[\w\.\-]{1,40}\$?)"""
    """exa_json_path=$.user.id,exa_field_name=user_sid"""  
  
}
```