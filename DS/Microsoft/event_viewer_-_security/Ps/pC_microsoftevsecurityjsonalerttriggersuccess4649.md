#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-alert-trigger-success-4649
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  ExtractionType = json
  Conditions = [ """"EventID":4649""", """"Message":"A replay attack was detected""", """Microsoft-Windows-Security-Auditing""", """"Channel":"Security"""" ]
  Fields = [
  """exa_json_path=$.EventTime,exa_field_name=time""",
  """exa_json_path=$.EventID,exa_field_name=event_code""",
  """exa_json_path=$.Hostname,exa_field_name=host""",
  """exa_json_path=$.Channel,exa_field_name=channel""",
  """exa_json_path=$.Message,exa_regex=({event_name}[^\.]+).\s*Subject""",
  """exa_json_path=$.EventType,exa_field_name=event_category""",
  """exa_json_path=$.SeverityValue,exa_field_name=alert_severity""",
  """exa_json_path=$.SourceName,exa_field_name=app""",
  """exa_json_path=$.ProviderGuid,exa_field_name=process_guid""",
  """exa_json_path=$.Task,exa_field_name=task_name""",
  """exa_json_path=$.OpcodeValue,exa_field_name=opcode""",
  """exa_json_path=$.RecordNumber,exa_field_name=event_id""",
  """exa_json_path=$.ActivityID,exa_field_name=activity_id""",
  """exa_json_path=$.ProcessID,exa_field_name=process_id""",
  """exa_json_path=$.ThreadID,exa_field_name=thread_id""",
  """exa_json_path=$.Category,exa_field_name=category""",
  """exa_json_path=$..SubjectUserSid,exa_field_name=user_sid""",
  """exa_json_path=$..SubjectUserName,exa_regex=^({user}[\w\.\-\!\#\^\~]{1,40}\$?)$""",
  """exa_json_path=$..SubjectDomainName,exa_field_name=domain""",
  """exa_json_path=$..SubjectLogonId,exa_field_name=login_id""",
  """exa_json_path=$.TargetUserName,exa_field_name=dest_user"""
  """exa_json_path=$.TargetDomainName,exa_field_name=dest_domain"""
  """exa_json_path=$.RequestType,exa_field_name=dns_query_type"""
  """exa_json_path=$..LogonProcessName,exa_regex=^(-|({auth_process}.+?))\s*$""",
  """exa_json_path=$.AuthenticationPackage,exa_field_name=auth_package"""
  """exa_json_path=$..ProcessName,exa_regex=^({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))$""",
  """exa_json_path=$..WorkstationName,exa_field_name=src_host_windows,exa_match_expr=!InList($.WORKSTATION_NAME,"-")"""
  ]
  DupFields = [ "event_name->alert_name", "auth_process->alert_type" ]
  ParserVersion = "v1.0.0"


}
```