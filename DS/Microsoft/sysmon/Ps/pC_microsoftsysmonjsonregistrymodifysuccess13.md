#### Parser Content
```Java
{
Name = microsoft-sysmon-json-registry-modify-success-13
  Vendor = Microsoft
  Product = Sysmon
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  ExtractionType = json
  Conditions = [ """"event_id":"13"""", """"provider_name":"Microsoft-Windows-Sysmon"""", """Registry value set""" ]
  Fields = [
    """exa_json_path=$.host,exa_field_name=host""",
    """exa_json_path=$..UtcTime,exa_field_name=time""",
    """exa_json_path=$.winlog.user.name,exa_regex=^({user}[\w\.\-\!\#\^\~]{1,40}\$?)$""",
    """exa_json_path=$.winlog.user.domain,exa_field_name=domain""",
    """exa_json_path=$.winlog.user.identifier,exa_field_name=user_sid""",
    """exa_json_path=$.winlog.event_id,exa_field_name=event_code""",
    """exa_regex=({event_name}Registry value set)""",
    """exa_json_path=$.winlog.event_data.ProcessGuid,exa_field_name=process_guid""",
    """exa_json_path=$.winlog.event_data.ProcessId,exa_field_name=process_id""",
    """exa_json_path=$.winlog.event_data.Image,exa_regex=^({process_path}({process_dir}[^",]*?)({process_name}[^\\",]+?))$""",
    """exa_json_path=$.winlog.event_data.TargetObject,exa_regex=^({file_path}({file_dir}[^",]*?)\s*({file_name}[^\\",]+?(\.({file_ext}\w+))?))$""",
    """exa_json_path=$.winlog.event_data.TargetObject,exa_field_name=registry_path""",
    """exa_json_path=$.winlog.event_data.RuleName,exa_field_name=rule""",
    """exa_json_path=$.winlog.event_data.EventType,exa_field_name=operation""",
    """exa_json_path=$.winlog.event_data.Details,exa_field_name=registry_value""",
    """exa_json_path=$.winlog.record_id,exa_field_name=event_id""",
    """exa_json_path=$.winlog.process.thread.id,exa_field_name=thread_id""",
    """exa_json_path=$.message,exa_field_name=additional_info""",
    """exa_json_path=$.winlog.provider_name,exa_field_name=provider_name""",
    """exa_json_path=$.winlog.task,exa_field_name=task_name"""
  ]
  ParserVersion = v1.0.0


}
```